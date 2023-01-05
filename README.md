# logstash

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&logoColor=white)](https://github.com/rolehippie/logstash) [![General Workflow](https://github.com/rolehippie/logstash/actions/workflows/general.yml/badge.svg)](https://github.com/rolehippie/logstash/actions/workflows/general.yml) [![Readme Workflow](https://github.com/rolehippie/logstash/actions/workflows/readme.yml/badge.svg)](https://github.com/rolehippie/logstash/actions/workflows/readme.yml) [![Galaxy Workflow](https://github.com/rolehippie/logstash/actions/workflows/galaxy.yml/badge.svg)](https://github.com/rolehippie/logstash/actions/workflows/galaxy.yml) [![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/logstash)](https://github.com/rolehippie/logstash/blob/master/LICENSE) ![Ansible Role](https://img.shields.io/ansible/role/55296)

Ansible role to install and configure a Logstash log processor.

## Sponsor

Building and improving this Ansible role have been sponsored by my current and previous employers like **[Cloudpunks GmbH](https://cloudpunks.de)** and **[Proact Deutschland GmbH](https://www.proact.eu)**.

## Table of content

- [Default Variables](#default-variables)
  - [logstash_exporter_args](#logstash_exporter_args)
  - [logstash_exporter_download](#logstash_exporter_download)
  - [logstash_exporter_enabled](#logstash_exporter_enabled)
  - [logstash_exporter_host](#logstash_exporter_host)
  - [logstash_exporter_port](#logstash_exporter_port)
  - [logstash_exporter_version](#logstash_exporter_version)
  - [logstash_extra_pipelines](#logstash_extra_pipelines)
  - [logstash_general_pipelines](#logstash_general_pipelines)
  - [logstash_group](#logstash_group)
  - [logstash_http_enabled](#logstash_http_enabled)
  - [logstash_http_host](#logstash_http_host)
  - [logstash_http_port](#logstash_http_port)
  - [logstash_initial_heap_space](#logstash_initial_heap_space)
  - [logstash_install_plugins](#logstash_install_plugins)
  - [logstash_java_home](#logstash_java_home)
  - [logstash_major_version](#logstash_major_version)
  - [logstash_maximum_heap_space](#logstash_maximum_heap_space)
  - [logstash_node_name](#logstash_node_name)
  - [logstash_openjdk_version](#logstash_openjdk_version)
  - [logstash_pipeline_ordered](#logstash_pipeline_ordered)
  - [logstash_repository](#logstash_repository)
  - [logstash_server_version](#logstash_server_version)
  - [logstash_user](#logstash_user)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

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
logstash_exporter_download: https://gitlab.com/alxrem/prometheus-logstash-exporter/uploads/e0e93259ae977cc73674b95e5f5b4cfa/prometheus-logstash-exporter-{{
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
logstash_exporter_version: 0.7.0
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

### logstash_major_version

Major version built via server version variable

#### Default value

```YAML
logstash_major_version: "{{ logstash_server_version.split('.')[0] }}"
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

### logstash_openjdk_version

Version of OpenJDK to install as part of Logstash

#### Default value

```YAML
logstash_openjdk_version: 11
```

### logstash_pipeline_ordered

Set the pipeline event ordering

#### Default value

```YAML
logstash_pipeline_ordered: auto
```

### logstash_repository

Repository used for installation

#### Default value

```YAML
logstash_repository: deb https://artifacts.elastic.co/packages/{{ logstash_major_version
  }}.x/apt stable main
```

### logstash_server_version

Version of Logstash that gets installed

#### Default value

```YAML
logstash_server_version: '8.5'
```

### logstash_user

Path to the java home environment

#### Default value

```YAML
logstash_user: logstash
```

## Discovered Tags

**_logstash_**

**_logstash-exporter_**


## Dependencies

- None

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
