

This project consists of 2 parts:
- Create K8s manifests for Deployments and Services for all microservices of an online shop application
- Deploy microservices to Linode's managed Kubernetes cluster

## Create K8s manifests for Deployments and Services for all microservices of an online shop application

Microservices Overview:

<img width="736" alt="Screenshot 2024-10-07 at 15 19 34" src="https://github.com/user-attachments/assets/8a63d1b0-73ff-4338-b9a1-e2682172c897">

<img width="880" alt="Screenshot 2024-10-07 at 15 20 29" src="https://github.com/user-attachments/assets/60991f5d-2e31-4e69-bdc2-3859d19851d9">

The manifests are written in config.yaml. For each microservice I've created a deployment (which ensures that there's always pods for that microservice) and a service to access the pod/s of that microsevice.

Each pod has environment variables to specify its port (and ports and other relevant info of any other microservice it needs to connect to).

## Deploy microservices app to Linode's managed Kubernetes cluster:


The config file that points to the cluster contains a secret key so it is recommended to modify its permissions to prevent unwanted users from accessing the cluster.

<img width="592" alt="Screenshot 2024-10-07 at 16 23 17" src="https://github.com/user-attachments/assets/e7ed128f-f4cc-442c-af8e-8aecfb118aad">

Afterwards, we configure kubectl to use the context in this new config file.
To ensure that it’s working we can get the pods currently running in the cluster (it should successfully connect and respond that there are no pods in the default namespace since we haven’t deployed anything)

<img width="595" alt="Screenshot 2024-10-07 at 16 26 41" src="https://github.com/user-attachments/assets/75c49e6b-085f-4d1d-8741-8a66558c5d3e">

Apply all the kubernetes resources defined in the config.yaml manifest:

<img width="549" alt="Screenshot 2024-10-07 at 16 24 11" src="https://github.com/user-attachments/assets/0be6c86d-8a17-46fd-ae6e-c16b79bd167c">

After a few seconds, we can check that all pods are running:

<img width="598" alt="Screenshot 2024-10-07 at 16 24 42" src="https://github.com/user-attachments/assets/d3780e87-53a3-4638-b213-ad87c10c3154">

we use one of the Node Pools IP addresses from Linode and port 30007 from the NodePort (frontend):

![image](https://github.com/user-attachments/assets/e0a3db9e-fd89-43e8-a56f-5abe5d1bf47b)

<img width="599" alt="Screenshot 2024-10-07 at 16 37 17" src="https://github.com/user-attachments/assets/6bc4e77d-7b10-4658-966c-5c2e5b152669">

This is the final website:

<img width="875" alt="Screenshot 2024-10-07 at 15 27 04" src="https://github.com/user-attachments/assets/a261ba37-11e7-468d-97a5-53643325bada">

