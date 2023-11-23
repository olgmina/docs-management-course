# Amedia
----------------

**Описание**:  Amedia would be a cross-platform library for work with media files, formats and codecs. This project based on ffmpeg.

  - **Технологический стек**: net-core 2.0
  - **Статус**:  0.0.15


## Зависимости

>= ffmpeg 4.4.4.4


## Конфигурация

Before usage configure environment:
~~~ csharp
    // Necessary
    AmediaStartup.Configure();
~~~

## Применение

VideoReader sample
~~~ csharp
    using (var reader = new VideoReader(source))
    {
        Frame frame = null;
        while ((frame = reader.GetNext()) != null)
        {
            // do work ...
        }
    }
~~~