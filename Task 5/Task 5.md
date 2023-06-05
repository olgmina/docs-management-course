Задание 1-2. Виды документов в процессе разработки ПО. Типы пользователей.

| Стадии | Документы | Типы пользователей |
| --- | --- | --- |
| Анализ требований | Спецификация бизнес-требований| Бизнес-аналитик |
|  | SRS | Системный аналитик |
|  | Техническое задание | Технический специалист |
| Проектирование архитектуры | Архитектурная спецификация | Архитектор |
| Детальное проектирование | Диаграмма классов | Разработчик |
|  | Разработка интерфейса | Дизайнер |
| Конструирование | Программный код | Программист |
| | Документация по API | Разработчик API |
| Комплексирование | Базовая конфигурация | Интегратор |
| Квалификационное тестирование | Документы о приемке | Тестировщик |
|  | Отчет о тестировании | Менеджер качества |

Задание 3. Найти актуальное определение понятия управления конфигурацией.

ГОСТ Р 59193-2020: Управление конфигурацией – это деятельность в области управления жизненным циклом изделия, направленная на обеспечение соответствия объекта конфигурации документации конфигурации, в том числе требованиям. Управление конфигурацией, согласно ГОСТ Р 57193-2016 (пункт 6.3.5), относится к процессам технического управления в ЖЦ системы.

Задание 4. Построить UML диаграмму процесса управления конфигурациями.

![ActivityDiagram](https://github.com/annaeve/docs-management-course/blob/main/Task%205/act_diagram.jpg)

Задание – [Исправить](https://github.com/annaeve/docs-management-course/blob/tasks-Doinikova/Task%205/qwest3.md) тесты.

Задание 5. Сравнительный анализ артефакторий. Артефактории (Artifact Repositories) – это инструменты, которые используются для хранения и управления бинарными файлами в отличии от систем контроля версий, такими как программные пакеты, библиотеки и другие зависимости. Примеры: MyGet, nmp, Индекс пакетов Python (PyPI).

| Criterion | Nexus | JFrog Artifactory | Apache Archiva | MyGet | nmp |
| --- | --- | --- | --- | --- | --- |
| License | Proprietary | Proprietary/Open Source | Open Source | Proprietary | Open Source |
| Supported package types | Java, Node.js, Ruby, Docker, Pyton, .NET, Golang | Java, Node.js, Ruby, Docker, Pyton, .NET, Golang, Perl, PHP, Chef, Puppet, CocoaPods, Gradle, Maven | Java, Node.js, Ruby, Pyton, Maven | NuGet, npm, Bower, VSIX, PowerShell, Python, RubyGems, Maven, Docker | Node.js-пакеты, nmp |
| Integration with CI/CD tools | Yes | Yes | Yes | Yes | Yes |
| Proxying and caching | Yes | Yes | Yes | Yes | No |
| Search functionality | Yes | Yes | Yes | Yes | Yes |
| User management | Yes | Yes | Yes | Yes | No |
| Content and access control | Yes | Yes | Yes | Yes | No |
| Security vulnerabilities scanning | Yes | Yes | No | Yes | No |
| REST API | Yes | Yes | Yes | Yes | Yes |
| Cost | Starts at $10/month | Starts at $39/month | Free | Starts at $1395/year | Free |
| Community support | Yes | Yes | Yes | Yes | Yes |

Задание 6. Архитектура системы контроля версий

| <!-- --> | <!-- --> |
|:-----:| :-----:|
| FUNC0 | связывание документа с его версиями |
| FUNC1 | добавление документа в набор |
| FUNC2 | проверка наличия документа в наборе |
| FUNC3 | сохранение прошлых версий |
| FUNC4 | сохранение идентификационных копий документа |
| FUNC5 | идентификация копий |
| FUNC6 | поиск копий и доступ к ним по идентификатору |
