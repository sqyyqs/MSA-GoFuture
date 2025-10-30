метрики

### бизнес

1) Количество заказов в минуту `'bookings_created_per_minute': 'rate(booking_created_total[1m])'`, ключевая бизнес-метрика отражающая состояние
   приложения.
2) Активные поездки `'active_trips': 'gauge'`
3) Отношение зарегистрированных поездок (не отмененных) ко всем созданным `'conversion_rate': 'booking_confirmed / booking_created'`
4) Отношение успешных платежей: `'payment_success_rate': 'payment_completed / payment_attempted'`

### технические

поскольку кафка – сердце EDA, то метрики этой подсистемы будут наиболее важными в эксплуатации

1) kafka_consumer_lag_max
2) kafka_broker_requests_processing_time_p99
3) kafka_topic_partitions_under_replicated
4) kafka_topic_unclean_leader_elections

### Другие немаловажные для контейнеров и сети

1) network_receive_bytes_per_second
2) container_memory_usage_bytes / container_memory_limit_bytes – процент потребляемой памяти

### Метрики flink

1) flink_task_backpressured_time_per_second 
2) flink_task_busy_time_per_second  
3) flink_task_num_records_in_per_second 
