Задание 1. Виды документов в процессе разработки ПО
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

Задание 2. Типы пользователей
Перечислены в таблице выше.

Задание 3. Управление конфигурацией - это процесс, направленный на эффективное управление конфигурацией программных средств в течение всего их жизненного цикла, включающий в себя определение, документирование, контроль, координацию и верификацию изменений в конфигурации программных средств.

Задание 4. Процесс управления конфигурациями
<!---
![image](https://user-images.githubusercontent.com/65451923/230900375-94036da9-cfd6-42d3-abf7-5b9d40559fe0.png)
--->

![configuration_management](https://github.com/anna5812m/docs-management-course/raw/amorgunova/picture/configuration_management.png)

Задание 5. Сравнительный анализ артефакторий

Artifact Repositories – это инструменты, которые используются для хранения и управления бинарными файлами в отличии от систем контроля версий, такими как программные пакеты, библиотеки и другие зависимости. Примеры: MyGet, nmp, Индекс пакетов Python (PyPI)
Результат - критерий /таблица
| Criterion | Nexus | JFrog Artifactory | Apache Archiva | MyGet | nmp | GitHub Packages |
| --- | --- | --- | --- | --- | --- | --- |
| License | Proprietary | Proprietary/Open Source | Open Source | Proprietary | Open Source | Open Source |
| Supported package types | Java, Node.js, Ruby, Docker, Pyton, .NET, Golang | Java, Node.js, Ruby, Docker, Pyton, .NET, Golang, Perl, PHP, Chef, Puppet, CocoaPods, Gradle, Maven | Java, Node.js, Ruby, Pyton, Maven | NuGet, npm, Bower, VSIX, PowerShell, Python, RubyGems, Maven, Docker | Node.js-пакеты, nmp | npm, Docker, NuGet, RubyGems, Maven, PyPI, PHP Composer |
| Integration with CI/CD tools | Yes | Yes | Yes | Yes | Yes | Yes |
| Proxying and caching | Yes | Yes | Yes | Yes | No | Yes |
| Search functionality | Yes | Yes | Yes | Yes | Yes | Yes |
| User management | Yes | Yes | Yes | Yes | No | Yes |
| Content and access control | Yes | Yes | Yes | Yes | No | Yes |
| Security vulnerabilities scanning | Yes | Yes | No | Yes | No | Yes |
| REST API | Yes | Yes | Yes | Yes | Yes | Yes |
| Cost | Starts at $10/month | Starts at $39/month | Free | Starts at $165/year | Free | Free |
| Community support | Yes | Yes | Yes | Yes | Yes | Yes |

Задание 6. Архитектура системы контроля версий

Задание 7. Составление план конфигурационного управления

Задание 8.
