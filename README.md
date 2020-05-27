# Prometheus_speedtest

Installs and configures the prometheus_speedtest exorter (https://github.com/jeanralphaviles/prometheus_speedtest)

## Requirements
* Python 3.7
* Virtualenv

## Role Variables
| Variable | Description | Default value |
| --- | --- | --- |
| `prometheus_speedtest_version` | The prometheus_speedtest version to install | `0.9.2` |
| `prometheus_speedtest_address` | The address to listen on | `0.0.0.0` |
| `prometheus_speedtest_port` | The port to listen on | `9516` |
| `prometheus_speedtest_flags` | String of extra flags for the `prometheus_speedtest` executable | `""` |
| `prometheus_speedtest_user` | The user to run as | `prom-speedtest` |
| `prometheus_speedtest_group` | The group of the user to run as | `{{ prometheus_speedtest_user }}` |

## Example Playbook
```yaml
- hosts: servers
  roles:
    - dmaes.prometheus_speedtest
```

## License
MIT
