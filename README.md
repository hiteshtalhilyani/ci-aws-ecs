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
