# spark-submit-eks-k8s-cluster
## Hello Springboot deployment using CICD Pipeline with helm

## Pre-requisites:
    - Install Java
    - Install Git
    - Install Maven
    - Install Docker
    - Install Jenkins
    - Install Helm
    - EKS Cluster
## Install Java:
    yum install java-1.8.0-openjdk-devel -y
## Install Git:
    yum install git -y
## Install Apache-Maven:
    wget https://mirrors.estointernet.in/apache/maven/maven-3/3.6.3/binaries/apache-maven-3.6.3-bin.tar.gz
    tar xvzf apache-maven-3.6.3-bin.tar.gz
    
    vi /etc/profile.d/maven.sh
    --------------------------------------------
    export MAVEN_HOME=/opt/apache-maven-3.6.3
    export PATH=$PATH:$MAVEN_HOME/bin
    --------------------------------------------
    
    source /etc/profile.d/maven.sh
    mvn -version
## Install Docker:
    yum install docker -y
    service docker start
    
