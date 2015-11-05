# Monasca-Log-Agent
Installs the Monasca-Log-Agent on a debian system.

## Requirements
JRE must be installed

## Configuration parameter

## Required
* monasca_log_api - Example: 192.168.10.4:8070
* keystone_host - Example: 192.168.10.5:5000
* username - Keystone username
* password - Keystone-user password
* project_name - project name of keystone-user
* domain_id - Keystone-user domain_id

### Optional Paramater
* dimensions - Add additional information

### installation required parameter
* base_dir_agent - a directory where monasca-log-agent is installed, defaults to '/opt'
* download_timeout - defines a time for timeout when downloading tar files
* logstash_agent_version - defines the logstash version to be installed
* logstash_agent_download - logstash base download url
* logstash_agent_dest - logstash base install path
* logstash_agent_conf_dir - a directory where logstash configuration files are stored
* logstash_agent_log_file - monasca-log-agent log file path