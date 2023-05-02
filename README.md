# ci-aws-ecs
Container CI using Jenkins, Nexus, AWS-ECS, Maven, Git, Sonarqube

# Tools Used
    1. Jenkins
    2. Nexus Repository
    3. Sonarqube
    4. Maven
    5. Git 
    6. Docker 
    7. ECR
    8. AWS CLI
    9. ECS

# Execution Flow
    1. Jenkins will fetch Latest code from Git/Github whenever their is commit
    2. Using Maven we will run Unit Test, Checkstyle and upload the result to sonarqube
    3. If Check passes, we will build tomcat based docker image which 
       will have JAVA Artifacts 
    4. Docker Image will be published to AWS ECR
    5. Latest image will be deployed to AWS ECS Cluster 

# Steps 
    1. Create Github webhook
    2. Create Dockerfiles 
    3. Prepare two separate Jenkinsfile one for stg and another for prod
    4. AWS Steps 
            1. IAM, ECR Repo Setup 
    5. Jenkins Steps 
            1. Install Plugins 
            2. Docker, Docker build & Publish
            3. Pipeline: aws steps
    6. Install Docker enginer & aws cli on jenkins
    7. Write Jenkinsfile for Build & publish image to ECR
    8. ECS Setup 
            1. ECS Cluster
            2. Task Definition
            3. Service 
    9. Code to Deploy Docker image to ECS 
    10. Repeat the step for PROD env after manual approval to deploy on ECS Cluster 
