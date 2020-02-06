# Enhanced Redis Exporter Dashboard for Kubernetes

This dashboard is forked from [oliver006/redis_exporter](https://github.com/oliver006/redis_exporter/blob/master/contrib/grafana_prometheus_redis_dashboard.json), aims to better experience while working with Kubernetes and Prometheus Operator.

## Notable Changes

- Allow switching datasources using the `$datasource` variable.
- Add variable `$service` to make the monitoring target human readable, instead of all cluster service IPs listed in `$instance`.
- Replace `label_values()` with `query_result(count_over_time(redis_up[$__range]))` for variable queries, which retrieves available options within the selected time range instead of latest.
- Some little layout changes.

## Preview

![](https://i.loli.net/2020/02/06/KjuvBrENebRqUwF.png)

## Downloads

The dashboard is available [here](./dashboard.json), as well as the [raw JSON file](https://raw.githubusercontent.com/wi1dcard/redis-exporter-dashboard/master/dashboard.json).
