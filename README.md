# work

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&logoColor=white)](https://github.com/rolehippie/graylog-sidecar) [![Testing Build](https://github.com/rolehippie/graylog-sidecar/workflows/testing/badge.svg)](https://github.com/rolehippie/graylog-sidecar/actions?query=workflow%3Atesting) [![Readme Build](https://github.com/rolehippie/graylog-sidecar/workflows/readme/badge.svg)](https://github.com/rolehippie/graylog-sidecar/actions?query=workflow%3Areadme) [![Galaxy Build](https://github.com/rolehippie/graylog-sidecar/workflows/galaxy/badge.svg)](https://github.com/rolehippie/graylog-sidecar/actions?query=workflow%3Agalaxy) [![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/graylog-sidecar)](https://github.com/rolehippie/graylog-sidecar/blob/master/LICENSE) 

Ansible role to install and configure the Graylog sidecar. 

## Sponsor 

[![Proact Deutschland GmbH](https://proact.eu/wp-content/uploads/2020/03/proact-logo.png)](https://proact.eu) 

Building and improving this Ansible role have been sponsored by my employer **Proact Deutschland GmbH**.

## Table of content

* [Default Variables](#default-variables)
  * [graylog_sidecar_api_token](#graylog_sidecar_api_token)
  * [graylog_sidecar_cache_path](#graylog_sidecar_cache_path)
  * [graylog_sidecar_config_directory](#graylog_sidecar_config_directory)
  * [graylog_sidecar_list_log_files](#graylog_sidecar_list_log_files)
  * [graylog_sidecar_log_path](#graylog_sidecar_log_path)
  * [graylog_sidecar_log_rotate_keep_files](#graylog_sidecar_log_rotate_keep_files)
  * [graylog_sidecar_log_rotate_max_file_size](#graylog_sidecar_log_rotate_max_file_size)
  * [graylog_sidecar_node_id](#graylog_sidecar_node_id)
  * [graylog_sidecar_node_name](#graylog_sidecar_node_name)
  * [graylog_sidecar_package](#graylog_sidecar_package)
  * [graylog_sidecar_send_status](#graylog_sidecar_send_status)
  * [graylog_sidecar_server_url](#graylog_sidecar_server_url)
  * [graylog_sidecar_tls_skip_verify](#graylog_sidecar_tls_skip_verify)
  * [graylog_sidecar_update_interval](#graylog_sidecar_update_interval)
  * [graylog_sidecar_whitelist](#graylog_sidecar_whitelist)
* [Dependencies](#dependencies)
* [License](#license)
* [Author](#author)

---

## Default Variables

### graylog_sidecar_api_token

Token for Graylog authentication

#### Default value

```YAML
graylog_sidecar_api_token:
```

### graylog_sidecar_cache_path

Cache path

#### Default value

```YAML
graylog_sidecar_cache_path: /var/cache/graylog-sidecar
```

### graylog_sidecar_config_directory

Path to config directory

#### Default value

```YAML
graylog_sidecar_config_directory: /var/lib/graylog-sidecar/generated
```

### graylog_sidecar_list_log_files

List log files

#### Default value

```YAML
graylog_sidecar_list_log_files: []
```

### graylog_sidecar_log_path

Log path

#### Default value

```YAML
graylog_sidecar_log_path: /var/log/graylog-sidecar
```

### graylog_sidecar_log_rotate_keep_files

Max files to keep for log rotation

#### Default value

```YAML
graylog_sidecar_log_rotate_keep_files: 10
```

### graylog_sidecar_log_rotate_max_file_size

Max file size for log rotation

#### Default value

```YAML
graylog_sidecar_log_rotate_max_file_size: 10MiB
```

### graylog_sidecar_node_id

Value of part for the node ID

#### Default value

```YAML
graylog_sidecar_node_id: file:/etc/machine-id
```

### graylog_sidecar_node_name

Node name sent to Graylog

#### Default value

```YAML
graylog_sidecar_node_name: '{{ inventory_hostname }}'
```

### graylog_sidecar_package

Download URL for sidecar package

#### Default value

```YAML
graylog_sidecar_package: https://github.com/Graylog2/collector-sidecar/releases/download/1.0.0/graylog-sidecar_1.0.0-1_amd64.deb
```

### graylog_sidecar_send_status

Send status

#### Default value

```YAML
graylog_sidecar_send_status: true
```

### graylog_sidecar_server_url

URL to Graylog server

#### Default value

```YAML
graylog_sidecar_server_url: http://127.0.0.1:9000
```

### graylog_sidecar_tls_skip_verify

Skip TLS verify

#### Default value

```YAML
graylog_sidecar_tls_skip_verify: false
```

### graylog_sidecar_update_interval

Update interval

#### Default value

```YAML
graylog_sidecar_update_interval: 10
```

### graylog_sidecar_whitelist

List of allowed binaries

#### Default value

```YAML
graylog_sidecar_whitelist:
  - /usr/bin/filebeat
  - /usr/bin/packetbeat
  - /usr/bin/metricbeat
  - /usr/bin/heartbeat
  - /usr/bin/auditbeat
  - /usr/bin/journalbeat
  - /usr/share/filebeat/bin/filebeat
  - /usr/share/packetbeat/bin/packetbeat
  - /usr/share/metricbeat/bin/metricbeat
  - /usr/share/heartbeat/bin/heartbeat
  - /usr/share/auditbeat/bin/auditbeat
  - /usr/share/journalbeat/bin/journalbeat
```

## Dependencies

* None

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
