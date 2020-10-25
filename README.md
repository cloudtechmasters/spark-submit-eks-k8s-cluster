# spark-submit-eks-k8s-cluster
## How to run Apache Spark on Kubernetes (Amazon EKS)

## Pre-requisites:
    - Install Java
    - Install Git
    - Install Maven
    - Install Docker
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
# EKS Cluster Setup:
  [EKS Cluster Setup](https://github.com/cloudtechmasters/eks-cluster-setup.git)
  
## Download Apache Spark 
    cd /opt
    wget https://mirrors.estointernet.in/apache/spark/spark-2.4.7/spark-2.4.7-bin-hadoop2.7.tgz
    tar xvf spark-2.4.7-bin-hadoop2.7.tgz
## Go to spark main directory
   cd spark-2.4.7-bin-hadoop2.7
   Execute build command. This command should be executed from Spark parent directory
   docker build -t cloudtechmasters/sparkimage:latest -f kubernetes/dockerfiles/spark/Dockerfile .
   
## Login to DockerHub Account
   docker login
   enter your username and password
## Push your sparkimage to dockerhub account
   docker push cloudtechmasters/sparkimage:latest
    
