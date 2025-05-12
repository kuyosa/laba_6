1. Написаны gateway.py и service.py - в gateway исправлена ошибка, что opentelemetry не подключалось по http порту.
2. Добавлены RabbitMQ - брокер собщений.
3. Добавлены Grafana для визуализации + Tempo для трассирования запросов.
4. Добавлен Prometheus для сбора метрик и мониторинга.
5. Добавлен RabbitMQ Exporter для сбора метрик RabbitMQ.
6. Добавлен и настроен Alertmanager для отправки уведовлений в чат тг.
7. Добавлены Node Exporter и cAdvisor для сбора метрик в системах мониторинга.