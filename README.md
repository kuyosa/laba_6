1) Создан RabbitMQ контейнер.
2) Разработка gateway:
    Отправка сообщений в RabbitMQ.
    Реализация логирования, обработки ошибок и повторных попыток подключения.
    Добавлена поддержка RPC (ответа от микросервиса).
    Генерация trace_id для распределённого трейсинга.
3) Разработка микросервиса:
    Получение сообщений из очереди.
    Обработка и отправка ответа обратно через RabbitMQ.
    Включено логирование и повторные подключения.
4) Реализация распределённого трейсинга:
    Интеграция OpenTelemetry.
    Первоначально подключён Jaeger, позже заменён на Grafana Tempo.
    trace_id передаётся через сообщения и отображается в UI.
5) Интеграция с Grafana:
    Интегрированна Grafana для визуального отображения различных метрик.
    В Grafana добавлены метрики Tempo и Prometheus.
6) Расширение мониторинга с Prometheus:
    Установка экспортёров.
    Интеграция метрик в сервисы.
7) Настройка алертов через Alertmanager:
    Отправка уведомлений в Telegram.
    Настройка цветовая маркировка сообщений.
8) Интеграция Node Exporter и cAdvisor
    Добавлены Node Exporter и cAdvisor для сбора метрик в системах мониторинга