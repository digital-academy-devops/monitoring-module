# Модуль 7. Системы мониторинга

Целью данного модуля является знакомство с компонентами системы мониторинга [Prometheus](https://prometheus.io/docs/prometheus/latest/getting_started/) и основами языка [PromQL](https://prometheus.io/docs/prometheus/latest/querying/basics/).

## Задание
1. При помощи docker-compose выполните локальное развертывание компонентов Prometheus.
   
   Для этого используйте [вариант кода развертывания](https://github.com/digital-academy-devops/monitoring-example#prometheus) рассмотренный на лекции.
2. Напишите запрос, подсчитывающий значение одной из метрик отображающих использование CPU и/или Памяти контейнерами.
3. Используя [оповещения Grafana](https://grafana.com/docs/grafana/latest/alerting/), создайте оповещение, срабатывающее при превышении результатом запроса некоего порогового значения.

## Рекомендации
- Для проверки корректности запроса, сравните получаемые значения с выводом [docker stats](https://docs.docker.com/engine/reference/commandline/stats/).
- Попробуйте реализовать запрос разными способами, с использование [операторов аггрегации](https://prometheus.io/docs/prometheus/latest/querying/operators/#aggregation-operators) и [rate](https://prometheus.io/docs/prometheus/latest/querying/functions/#rate)/[irate](https://prometheus.io/docs/prometheus/latest/querying/functions/#irate), либо [функции аггрегации по времени](https://prometheus.io/docs/prometheus/latest/querying/functions/#aggregation_over_time).
- Пороговое значение можете определить индивидуально, в зависимости от запущенных локально контейнеров. Допускается использование тестового контейнера реализуюзщего выраженную нагрузку. 
