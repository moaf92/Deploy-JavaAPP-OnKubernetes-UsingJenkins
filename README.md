# Deploy-JavaAPP-OnKubernetes-UsingJenkins


# Steps To Follow
- create three ec2 instances and configure them as nodes for our cluster one master and two worker nodes with security group

- create two ec2 instances one as sonarqube sever and the other one for nexus, install docker on both servers, and create a docker container for sonar and nexus from pulling images from dockerhub, we will use 'docker exec' command to execute commands from inside the container to obtain the nexus pass

- now for jenkins we will also install one ec2 instance,for setup jenkins server it has prerequisite to install java on jenkins server and we will also install docker and trivy to scan our source code to find any vulnerability that may exist in the dependencies we are using 

- now time to install some plugins on our jenkins server 'eclips temurin installer'to install multiple versions of jdk, pipeline maven integration, sonarqube scanner, docker, docker pipeline, kubernetes

- next time to configure tools on jenkins globally 'jdk,maven,sonar,docker'

- now time for our pipeline but before we  have to set some credentials to deal with tools that we want to integrate with jenkins by setting pass and tokens

- Deploy our app on k8s cluster, but first we are going to create rbac to set some rules and permissions to specific users, by creating service account with a seperate user, and attach role to it, by creating roleBinding 

- now time to make jenkins connect to our cluster by creating a token for authentication and save it in jenkins credentials and install kubectl utility on jenkins server

- after that set email notification by setting app password as atoken and configure it at jenkins as extended email notification

- now time to set up a monitoring server to install prometheus and grafana and blackbox exporter, and configure prometheus as a data source for grafana, and set up blackbox grafana dashboard to monitor the webapp itself

- last step install node exporter on jenkins server to monitor system metrics



