# FCS Tools

Super high level quick overview of the tools we'll likely be using in the competition.

## ELK Stack

The ELK stack (aka Elastic stack) is a collection of tools commonly used together for log analysis/management.

The core components of the ELK stack are [Elasticsearch](https://www.elastic.co/guide/en/elasticsearch/reference/current/index.html), [Kibana](https://www.elastic.co/guide/en/kibana/current/index.html), and [Logstash](https://www.elastic.co/guide/en/logstash/current/introduction.html).

The ELK stack is highly customizable and there are often many other tools used to fit an organizations needs.

### Elasticsearch

Elasticsearch is the heart of the ELK stack. It both stores all of the log data and provides an interface for queries.

### Kibana

Kibana provides customizable visual dashboards to analyze Elasticsearch data.

### Logstash

Logstash acts as the data pipeline from endpoints into Elasticsearch. It uses a combination of Inputs, Filters, and Outputs to achieve this.

#### Inputs

Inputs are the endpoints that generate data. Logstash offers a range of [plugins](https://www.elastic.co/guide/en/logstash/current/input-plugins.html) from which data can be ingested.

#### Filters

Filters allow you to format data as it's ingested.

Some use [case examples](https://www.elastic.co/logstash#react-tabs-2).

- Derive structure from unstructured data with grok
- Decipher geo coordinates from IP addresses
- Anonymize PII data, exclude sensitive fields completely
- Ease overall processing, independent of the data source, format, or schema.

#### Outputs

Outputs are the destinations that Logstash supports sending ingested data to.

In ELK stack the output is Elasticsearch.

### ELK Stack Resources

- [Official Site](https://www.elastic.co/elastic-stack/)
- [Documentation](https://www.elastic.co/docs)

#### Preferred Operating Systems

#### Installation

- [ELK Stack Installation Guide](https://www.elastic.co/guide/en/elastic-stack/current/installing-stack-demo-self.html)
- [Elasticsearch Download](https://www.elastic.co/downloads/elasticsearch)
- [Kibana Download](https://www.elastic.co/downloads/kibana)
- [Logstash Download](https://www.elastic.co/downloads/logstash)
- [Elasticsearch Docker](https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html)
- [Kibana Docker](https://www.elastic.co/guide/en/kibana/current/docker.html)
- [Logstash Docker](https://www.elastic.co/guide/en/logstash/current/docker.html)

## Wazuh

Wazuh is an open source SIEM.

The core components of Wazuh are the [Agent](https://documentation.wazuh.com/current/user-manual/agent/index.html), [Indexer](https://documentation.wazuh.com/current/user-manual/wazuh-indexer/index.html), [Server](https://documentation.wazuh.com/current/user-manual/manager/index.html), and [Dashboard](https://documentation.wazuh.com/current/user-manual/wazuh-dashboard/index.html).

### Wazuh Agent

Wazuh agents are the software running on the endpoints from which data is collected.

### Wazuh Indexer

The indexer is Wazuh's search and analysis engine. It stores the data collected from the agents.

### Wazuh Server

The Wazuh server is responsible for managing and analyzing the data sent from the agents.

### Wazuh Dashboard

The web interface used to interact with the Wazuh server.

### Wazuh Resources

- [Official Site](https://wazuh.com/)
- [Documentation](https://documentation.wazuh.com/current/index.html)

#### Recommended Operating Systems

- Amazon Linux 2, Amazon Linux 2023
- CentOS 7, 8
- Red Hat Enterprise Linux 7, 8, 9
- Ubuntu 16.04, 18.04, 20.04, 22.04, 24.04

#### Installation

- [Wazuh Agent Installation](https://documentation.wazuh.com/current/installation-guide/wazuh-agent/index.html)
- [Wazuh Indexer Installation](https://documentation.wazuh.com/current/installation-guide/wazuh-indexer/index.html)
- [Wazuh Server Installation](https://documentation.wazuh.com/current/installation-guide/wazuh-server/index.html)
- [Wazuh Dashboard Installation](https://documentation.wazuh.com/current/installation-guide/wazuh-dashboard/index.html)

## Arkime

Arkime is a packet capture and network analysis tool.

[Arkime supports integration with elasticsearch.](https://arkime.com/faq#elasticsearch)

### Arkime Resources

- [Official Site](https://arkime.com/)
- [Documentation](https://arkime.com/learn)

#### Recommended Operating Systems
- Amazon Linux 2, Amazon Linux 2023
- Arch
- Debian 12
- EL 8, 9
- Ubuntu 20.04, 22.04, 24.04

#### Installation

- [Download](https://github.com/arkime/arkime/releases/tag/v5.4.0)

## Velociraptor

Open source endpoint monitoring and DFIR tool.

### Resources

- [Official Site](https://www.rapid7.com/products/velociraptor/)
- [Documentation](https://docs.velociraptor.app/docs/)

#### Installation

- [Download](https://github.com/Velocidex/velociraptor/releases/)
