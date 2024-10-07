# Deploy MS application in K8s Provide Git URL

This project consists in 2 parts:
- Create K8s manifests for Dpeloyments and Services for all microservices of an online shop application
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
