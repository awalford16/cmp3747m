# Gcloud Deployment Manager

Using Google Cloud's deployment manager, this code deploys various cloud resources utilising IaaS and PaaS. Main configuration file is written in yaml and all template files are written in Jinja2.

The deployment is configured to manage IoT devices without the use of IoT core.

To deploy on Gcloud:

    // In directory containing config.yaml
    gcloud deployment-manager deployments create DEPLOYMENT_NAME --config config.yaml

## What does the deployment include?

- Regional managed instance group for users to connect to front-end web services
- Regional managed instance group for IoT devices to connect to back-end
- CloudSQL with Users DB
- Cloud Storage bucket for IoT data
- Subnets and firewall rules for front-end and back-end devices
- Load balancer to manage traffic coming into front-end web services
- VPN tunnel between IoT devices and back-end network
