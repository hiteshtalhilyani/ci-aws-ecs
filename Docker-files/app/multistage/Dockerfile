FROM openjdk:8 AS BUILD_IMAGE
RUN apt update && apt install maven -y
RUN git clone https://github.com/hiteshtalhilyani/jenkins-cicd.git
RUN cd jenkins-cicd
RUN mvn install 


