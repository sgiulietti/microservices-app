## DEMO MICROSERVICES APP WITH K8S ON DIGITAL OCEAN
 Prerequisites: Have an account on Digital Ocean cloud provider.

 ### MongoDB

 Step 1: Create a config yaml file that contains the deployment and service configuration for each microservice of an online shop example: https://github.com/GoogleCloudPlatform/microservices-demo

 Step 2: Create from DO UI a kubernetes cluster.

 Step 3: Install the kubernetes official client and DO command-line tool, “doctl” , to interact with and manage clusters.

Step 4: Change permissions on config.yaml file only for your user for security best practices.
Execute the following command:

    chmod 400 config.yaml

Step 5: Create a namespace for deploying the microservices.
Execute the following command:

    kubectl create ns myns

Step 6: Deploy the microservices into the new namespace.
Execute the following command:

    kubectl apply -f config.yaml -n mysn

Step 7: Deploy the microservices into the new namespace.
Execute the following command:

    kubectl apply -f config.yaml -n mysn    

### IMPLEMENTED BEST PRACTICES

Fixed version of any image used.
Liveness probe.
Readiness probe.
Resource request.
Resource limits.
Implement LoadBalancer service type instead of exposing NodePort.
Implement more than 1 replica for deployment.
