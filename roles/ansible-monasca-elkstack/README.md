# Monasca ELKstack
Installs and configures the following Monasca ELK components on one machine:
* ElasticSearch
* Kibana
* Logstash
* monasca-log-transformer
+ monasca-log-persister

The relevant services will be started.

## Required Variables
* kafka_hosts - Example: 192.168.10.4:9092
* zookeeper_hosts - Example: 192.168.10.4:2181

## Optional
* log_dir - base directory where logs are saved to
* elk_base_dir - a directory where ELK components are installed, defaults to '/opt'
* download_timeout - defines a time for timeout when downloading ELK tar files, defaults to 600
* elasticsearch_version - defines the elasticsearch version to be installed, defaults to '1.5.1'
* logstash_version - defines the logstash version to be installed, defaults to '1.5.0'
* logstash_conf_dir - a directory where logstash configuration files are stored, defaults to '/etc/monasca/log'
* log_topic - defines the Kafka topic id between  monasca-log-api and transformer, defaults to 'log'
* tranformed_log_topic - defines the Kafka topic id between transformer and persister, defaults to 'transformed-log'

### Kibana
* kibana_version - defines the kibana version to be installed, defaults to '4.1.2-linux-x64'
* kibana_log_dir - defines location for log file, defaults to {{ log_dir }}/kibana
* kibana_log_level - defines log level for kibana, defaults to 'debug'
