# 🚀 Setup pipeline using CircleCI, update GitHub Kubernetes manifest repo and push image on Docker

✨This repository containe the code of the kubernetes manifest files.

## 🏠 Architecture
![Architecture of the application](architecture.gif)

## 💶 Notes and Links
**I've divided my Blog into four parts**
this is the 3rd part of the project. Please go through below blog to get more idea

- 3rd Blog: [🔗 Links](https://www.showwcase.com/show/35857/setup-pipeline-using-circleci-update-github-kubernetes-manifest-repo-and-push-image-on-docker)

## 🔶 Story
- When CircleCI notices any changes in the application code, it starts executing the jobs that we have set up. There are a total of four jobs:

### 🧪 Test: 
- This job tests the code. After the test job is completed, CircleCI proceeds to the next job. 
- Note: I didn't add this job to save time. 😎

### 🏗️ Build: 
- In the build job, CircleCI pulls the base Docker images and packages our application code inside the image.

### 🪠 Push: 
- The push job pushes the newly generated images to Docker Hub with a new tag.

### 🆕 Update Manifest: 
- After the successful completion of the push job, the last job is executed, which updates the Kubernetes manifest repository with the new tag. This enables ArgoCD to detect the change and apply it to the cluster.

By following this pipeline, we ensure that our application code is thoroughly tested, built into Docker images, and deployed with the updated manifest using the GitOps approach.


## 💶 Links

- 1st Blog: [🔗 Links](https://www.showwcase.com/show/35840/deploying-dockerized-app-on-aws-eks-cluster-using-argocd-and-gitops-methodology-with-circleci)

- 2nd Blog: [🔗 Links](https://www.showwcase.com/show/35778/provisioning-the-amazon-eks-cluster-using-terraform)

- 4th Blog: [🔗 Links](https://www.showwcase.com/show/35858/install-argocd-on-the-eks-cluster-and-configure-sync-with-github-manifest-repository)



**This blog containe Three GitHub repository**
- Application code repo    ➡️ Containe application code [Links](https://github.com/AnkitJodhani/Todo_application.git)

- Terraform code repo      ➡️ Provisioning Amazon EKS Cluster using Terraform [Links](https://github.com/AnkitJodhani/kube_terraform-4thWeekOfCloudOps.git)

- Kubernetes manifest repo ➡️ this one

If you want to learn how i created this project, please go through my blogs. I've shared link of all the blogs above.👆

🙏 Thank you so much for reading..



[![Provisioning EKS cluster using terraform](https://project-assets.showwcase.com/110249/1688914154356-AWS%2520EKS.gif)](https://www.showwcase.com/show/35778/provisioning-the-amazon-eks-cluster-using-terraform)

[![Setup pipeline using CircleCI, update GitHub Kubernetes manifest repo and push image on Docker](https://project-assets.showwcase.com/110249/1688975395510-git%252Bkubernetes%252Bcircleci.gif)](https://www.showwcase.com/show/35857/setup-pipeline-using-circleci-update-github-kubernetes-manifest-repo-and-push-image-on-docker)

[![Install ArgoCD on the EKS cluster and configure sync with GitHub manifest repository](https://project-assets.showwcase.com/110249/1688982849073-argocd_sync.gif)](https://www.showwcase.com/show/35858/install-argocd-on-the-eks-cluster-and-configure-sync-with-github-manifest-repository)


