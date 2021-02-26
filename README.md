# logstash

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&logoColor=white)](https://github.com/rolehippie/logstash) [![Build Status](https://img.shields.io/drone/build/rolehippie/logstash/master?logo=drone)](https://cloud.drone.io/rolehippie/logstash) [![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/logstash)](https://github.com/rolehippie/logstash/blob/master/LICENSE) 

Ansible role to install and configure a Logstash log processor. 

## Sponsor 

[![Proact Deutschland GmbH](https://proact.eu/wp-content/uploads/2020/03/proact-logo.png)](https://proact.eu) 

Building and improving this Ansible role have been sponsored by my employer **Proact Deutschland GmbH**.

## Table of content

* [Default Variables](#default-variables)
  * [logstash_exporter_args](#logstash_exporter_args)
  * [logstash_exporter_download](#logstash_exporter_download)
  * [logstash_exporter_enabled](#logstash_exporter_enabled)
  * [logstash_exporter_host](#logstash_exporter_host)
  * [logstash_exporter_port](#logstash_exporter_port)
  * [logstash_exporter_version](#logstash_exporter_version)
  * [logstash_extra_pipelines](#logstash_extra_pipelines)
  * [logstash_general_pipelines](#logstash_general_pipelines)
  * [logstash_group](#logstash_group)
  * [logstash_http_enabled](#logstash_http_enabled)
  * [logstash_http_host](#logstash_http_host)
  * [logstash_http_port](#logstash_http_port)
  * [logstash_initial_heap_space](#logstash_initial_heap_space)
  * [logstash_install_plugins](#logstash_install_plugins)
  * [logstash_java_home](#logstash_java_home)
  * [logstash_maximum_heap_space](#logstash_maximum_heap_space)
  * [logstash_node_name](#logstash_node_name)
  * [logstash_pipeline_ordered](#logstash_pipeline_ordered)
  * [logstash_repository](#logstash_repository)
  * [logstash_server_version](#logstash_server_version)
  * [logstash_user](#logstash_user)
* [Dependencies](#dependencies)
* [License](#license)
* [Author](#author)

---

## Default Variables

### logstash_exporter_args

List of arguments joined for the executable

#### Default value

```YAML
logstash_exporter_args: []
```

### logstash_exporter_download

URL to the archive of the release to install

#### Default value

```YAML
logstash_exporter_download: https://gitlab.com/alxrem/prometheus-logstash-exporter/uploads/2b66e95552dcd921fbbf667bb2e46cf3/prometheus-logstash-exporter-{{
  logstash_exporter_version }}-linux-amd64
```

### logstash_exporter_enabled

Enable the logstash exporter

#### Default value

```YAML
logstash_exporter_enabled: true
```

### logstash_exporter_host

Host of logstash to connect to

#### Default value

```YAML
logstash_exporter_host: localhost
```

### logstash_exporter_port

Port of logstash to connect to

#### Default value

```YAML
logstash_exporter_port: 9600
```

### logstash_exporter_version

Version of the release to install

#### Default value

```YAML
logstash_exporter_version: 0.6.2
```

### logstash_extra_pipelines

List of extra pipeline definitions

#### Default value

```YAML
logstash_extra_pipelines: []
```

### logstash_general_pipelines

List of general pipeline definitions

#### Default value

```YAML
logstash_general_pipelines:
  - pipeline.id: main
    path.config: /etc/logstash/conf.d/*.conf
```

### logstash_group

Name of the group owning Elasticsearch

#### Default value

```YAML
logstash_group: logstash
```

### logstash_http_enabled

Enable the integrated HTTP API

#### Default value

```YAML
logstash_http_enabled: true
```

### logstash_http_host

Host binding for the HTTP API

#### Default value

```YAML
logstash_http_host: 127.0.0.1
```

### logstash_http_port

Port range for the HTTP API

#### Default value

```YAML
logstash_http_port: 9600-9700
```

### logstash_initial_heap_space

Represents the initial size of total heap space

#### Default value

```YAML
logstash_initial_heap_space: 1g
```

### logstash_install_plugins

List of plugins to install

#### Default value

```YAML
logstash_install_plugins: []
```

### logstash_java_home

#### Default value

```YAML
logstash_java_home: /usr/lib/jvm/java-11-openjdk-amd64
```

### logstash_maximum_heap_space

Represents the maximum size of total heap space

#### Default value

```YAML
logstash_maximum_heap_space: 1g
```

### logstash_node_name

Name of the node

#### Default value

```YAML
logstash_node_name: '{{ ansible_hostname }}'
```

### logstash_pipeline_ordered

Set the pipeline event ordering

#### Default value

```YAML
logstash_pipeline_ordered: auto
```

### logstash_repository

Dict of repositories matching the choosen version

#### Default value

```YAML
logstash_repository:
  '7.8': deb https://artifacts.elastic.co/packages/7.x/apt stable main
```

### logstash_server_version

Version of Logstash that gets installed

#### Default value

```YAML
logstash_server_version: '7.8'
```

### logstash_user

Path to the java home environment

#### Default value

```YAML
logstash_user: logstash
```

## Dependencies

* None

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
