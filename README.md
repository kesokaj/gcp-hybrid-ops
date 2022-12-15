# google-operations-logs-and-metrics

## Google Logging Agent
### 1.) Install logging agent on vm or physical machine
````
curl -sSO https://dl.google.com/cloudagents/add-logging-agent-repo.sh
sudo bash add-logging-agent-repo.sh --also-install
````

### 2.) Add service account key-file.
````
a.) Create serviceaccount with these permissions
https://www.googleapis.com/auth/logging.write
b.) Export key as json
c.) Move key to fluentd machine /etc/google/auth/application_default_credentials.json and chmod 0400 and user root:root
````
## Google Managed Prometheus
### 1.)
````
Run docker-compose.yaml file and edit config.yaml to your own parameters.
````
### 2.)
````
a.) Create serviceaccount with these permissions
https://www.googleapis.com/auth/metric.writer
b.) Export key as json
c.) - '--export.credentials-file=/gmp/key.json' 
````
