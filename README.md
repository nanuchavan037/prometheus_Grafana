# prometheus_Grafana

## Prerequisites:

   1  Docker and Docker Compose installed on your system
   2 The application must expose metrics in a format Prometheus understands (e.g., /metrics endpoint)

## Steps:
## Step 1: Setting Up Prometheus and Grafana using Docker Compose

 ### Create a "[docker-compose.yml]" file to define services for Prometheus and Grafana.

## Step 2: Configure Prometheus

### In the prometheus service, create a [prometheus.yml] file inside a folder named prometheus in your project directory. Configure scrape configs to collect metrics from your application. 

## Step 3: Start Prometheus and Grafana

### Run the following command in your terminal:

```bash

docker-compose up -d
```

### This will start Prometheus and Grafana in the background.

## Step 4: Validate the Configuration

### Access Prometheus UI by visiting http://localhost:9090 in your browser. Go to the 'Status' and 'Targets' tabs to check if your application job is listed and shows UP status.

## Step 5: Connect Grafana to Prometheus

### Access Grafana by visiting http://localhost:3000 in your browser. Log in using the default username admin and the password you set in the docker-compose.yml.

    Add Prometheus as a datasource in Grafana.
    Go to Configuration > Data Sources > Add data source.
    Select Prometheus and configure it with http://prometheus:9090 (the service name in the docker network) as the URL.

## Step 6: Create Dashboards in Grafana

### Create a new dashboard in Grafana:

    Go to Create > Dashboard > Add new panel.
    Select the data source as the Prometheus data source you added.
    Build your panels and queries based on the metrics provided by your application.
