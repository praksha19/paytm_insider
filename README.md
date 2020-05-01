# paytm_insider

#### Assessment 

* steps:

1. first i have installed a minikube in my local machine
2. As per the inststructions given i have create a deployment of nodejs image where i have taken from docker hub.
Note: . As mentioned i was not able to find any nodejs-test:latest docker image in ECR on AWS
      . I was not able to able to create a EC2 instance in the aws because i have a free account but the 
        configuration was not sufficent to install minikube or kops in AWS because it is chargable.
3. The deployment should autoscale at average 50% cpu and 60% memory: i have attached the yaml file for both cpu and memory 
   and test results has been attached.
4. while cpu and memory reached more that 50% and 60% the pods will spin up 10 replicas attached the screenshots.
5. Any change to the deployment should always ensure at least 7 replicas are running at all times: yes onec the cpu and memory
   come to required limit it will run only 7.
6. Should have higher priority than daemonset pods: attached yaml files for priority 
7. Tested load and shared the results.
8. i have used minikube tunneling to expose the service which is running on port 3000
 Note: i was unable to use the EC2 classic load balancer because i dnt have sufficent resource in aws.
