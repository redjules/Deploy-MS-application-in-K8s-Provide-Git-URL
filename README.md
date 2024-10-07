# Deploy MS application in K8s Provide Git URL

This project consists in 2 parts:
- Create K8s manifests for Deployments and Services for all microservices of an online shop application
- Deploy microservices to Linode's managed Kubernetes cluster

  
This is an overview of the project:

<img width="463" alt="Screenshot 2024-10-07 at 15 10 22" src="https://github.com/user-attachments/assets/26e9cbe7-11df-4545-861c-37a76e8056d9">

we create a Kubernetes cluster with Linode, a cloud hosting provider that focused on providing Linux-based virtual machines, cloud infrastructure, and managed services:

<img width="464" alt="Screenshot 2024-10-07 at 15 11 50" src="https://github.com/user-attachments/assets/7e53a3a1-a71c-4fa6-aa6b-7a0eb659ccca">


<img width="887" alt="Screenshot 2024-10-07 at 15 12 17" src="https://github.com/user-attachments/assets/dd38ec1d-6f4d-4afe-ace7-ad5da313e7c3">

we choose node pools of 4GB:

<img width="885" alt="Screenshot 2024-10-07 at 15 13 36" src="https://github.com/user-attachments/assets/d31886f6-a5c7-4c2a-956e-fb637a6f6c69">

we download the kubeconfig.yaml, add it to the folder with the 

<img width="889" alt="Screenshot 2024-10-07 at 15 14 09" src="https://github.com/user-attachments/assets/44e77512-2aa3-43c1-b6e2-cb42360f4e6c">


# Deploy microservices app:

<img width="736" alt="Screenshot 2024-10-07 at 15 19 34" src="https://github.com/user-attachments/assets/8a63d1b0-73ff-4338-b9a1-e2682172c897">

<img width="880" alt="Screenshot 2024-10-07 at 15 20 29" src="https://github.com/user-attachments/assets/60991f5d-2e31-4e69-bdc2-3859d19851d9">

The config file that points to the cluster contains a secret key so it is recommended to modify its permissions to prevent unwanted users from accessing the cluster.

<img width="592" alt="Screenshot 2024-10-07 at 16 23 17" src="https://github.com/user-attachments/assets/e7ed128f-f4cc-442c-af8e-8aecfb118aad">

Afterwards, we configure kubectl to use the context in this new config file.
To ensure that it’s working we can get the pods currently running in the cluster (it should successfully connect and respond that there are no pods in the default namespace since we haven’t deployed anything)

<img width="593" alt="Screenshot 2024-10-07 at 16 23 49" src="https://github.com/user-attachments/assets/98ea483d-ea46-4124-98ab-88dfb88cca85">

Apply all the kubernetes resources defined in the config.yaml manifest:![image](https://github.com/user-attachments/assets/7a6a00f6-6ec0-445b-91db-f3b63942274d)

<img width="549" alt="Screenshot 2024-10-07 at 16 24 11" src="https://github.com/user-attachments/assets/0be6c86d-8a17-46fd-ae6e-c16b79bd167c">

After a few seconds, we can check that all pods are running:

<img width="598" alt="Screenshot 2024-10-07 at 16 24 42" src="https://github.com/user-attachments/assets/d3780e87-53a3-4638-b213-ad87c10c3154">

<img width="875" alt="Screenshot 2024-10-07 at 15 27 04" src="https://github.com/user-attachments/assets/a261ba37-11e7-468d-97a5-53643325bada">

