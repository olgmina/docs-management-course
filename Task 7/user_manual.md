
# **Prerequirements** #
// on local machine
- скомпилированные файлы ПО Страж
- скомпилированные файлы Angel Vision
- лицензия для Angel Vision
опционально
- wsl -> rsync

// on remote machine
- Postgresql
- Текстовый редактор

# На удаленной машине: #
- устанавливаем Postgresql и nano 
<pre><code># sudo apt install postgresql </code></pre>
<pre><code># sudo apt install </code></pre>
### Настраиваем postgres ###
- устанавливаем пароль для "postgres"
<pre><code># sudo su - postgres </code></pre>
<pre><code># psql -c "ALTER USER postgres WITH PASSWORD 'postgres';" </code></pre>
<pre><code># exit </code></pre>
- меняем порт на 4321 в файле postgresql.conf "port = 4321"
<pre><code># sudo vi /etc/postgresql/11/main/postgresql.conf </code></pre>
or 
<pre><code># sudo nano /etc/postgresql/11/main/postgresql.conf </code></pre>
- restart service    
<pre><code># sudo systemctl restart postgresql.service </code></pre>

### Создаем папку для ПО ###
<pre><code># sudo mkdir /opt/strazh/ </code></pre>
<pre><code># sudo mkdir /opt/angel_vision_3/ </code></pre>
<pre><code># sudo mkdir /opt/angel_vision_3/license/ </code></pre>

### Конфигурируем владельца ###
<pre><code># sudo chown -R linaro:root /opt/strazh && sudo chmod -R go-w /opt </code></pre>
<pre><code># sudo chown -R linaro:root /opt/angel_vision_3/ </code></pre>

# На локальной машине: #
### Копируем скомпилированные файлы. Любым удобным способом. ###
- Пример через rsync если порт отличается от 22
<pre><code># rsync -arvz -e "ssh -p 65123" --progress ./publish/ linaro@<ip>:/opt/strazh </code></pre>
- Дефолтный порт
<pre><code># rsync -arvz --progress ./publish/ root@<ip>:/opt/strazh </code></pre>
<pre><code># rsync -arvz --progress ./angel_vision_3/ linaro@<ip>:/opt/angel_vision_3/ </code></pre>
<pre><code># rsync -arvz --progress ./license/ linaro@<ip>:/opt/angel_vision_3/license/ </code></pre>

# На удаленной машине #
### Конфигурируем владельца ###
<pre><code># sudo chown -R linaro:root /opt/strazh && sudo chmod -R go-w /opt </code></pre>
### Настройка Angel Vision ###
- конфигурируем папки для поиска разделяемых библиотек
<pre><code># sudo echo "/opt/angel_vision_3/lib/" > /etc/ld.so.conf.d/angel-vision.conf </code></pre>
- создаем ссылку для связи с определенной версией Angel Vision
<pre><code># cd /opt/angel_vision_3/lib/ </code></pre>
<pre><code># ln -s libav_lpr_c_<version>.so libav_lpr_c.so </code></pre>
- обновляем список разделяемых библиотек
<pre><code># sudo /sbin/ldconfig </code></pre>
- проверяем что Angel Vision загружен 
<pre><code># cd /opt/angel_vision_3/lib/ </code></pre>
<pre><code># ldd libav_lpr_c.so </code></pre>
- копируем лицензию 
<pre><code># sudo cp /opt/angel_vision_3/license/* /opt/strazh/ </code></pre>

// configure.sh попадается с не корректными переносами
- поправляем
<pre><code># sed -i.bak 's/\r$//' /opt/strazh/configure.sh </code></pre>
- создаем демона
<pre><code># sudo /opt/strazh/configure.sh -name Strazh -workingdirectory /opt/strazh -y </code></pre>
- reload \-> enable \-> start
<pre><code># sudo systemctl daemon-reload </code></pre>
<pre><code># sudo systemctl enable Strazh </code></pre>
<pre><code># sudo systemctl restart Strazh </code></pre>