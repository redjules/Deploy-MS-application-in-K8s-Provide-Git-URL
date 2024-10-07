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

<img width="869" alt="Screenshot 2024-10-07 at 15 21 08" src="https://github.com/user-attachments/assets/a50f3f4b-c22f-45cd-974c-8b41efc74e0d">

<img width="838" alt="Screenshot 2024-10-07 at 15 21 32" src="https://github.com/user-attachments/assets/7f58e9bf-86ea-4116-b8f9-22b80c0adc4a">



<img width="885" alt="Screenshot 2024-10-07 at 15 22 29" src="https://github.com/user-attachments/assets/5c7590a6-3fe8-49ca-b529-99c805829282">


<img width="883" alt="Screenshot 2024-10-07 at 15 22 59" src="https://github.com/user-attachments/assets/9478453a-7f19-4be2-8fcb-b2b3ea16a9d6">
