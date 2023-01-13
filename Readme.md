Steps followed to execute the project:

1) Prerequisites 
- Azure Subscription
- VS code (Optional)
- Terraform  
- HELM

2) Terraform code For aks cluster:
- provider.tf
  Includes information of provider (azurerm)
- variables.tf
  mentions the variables used in main code
- Terraform.tfvars
  Define values for the vatiables
- Output.tf
  Includes cluster information which will be shown after the cluster is deployed.
- main.tf
  Includes 3 resources groups and information of cluster with 2 worker nodes
-Links used for help: 

3) Manifest file for deployment
- Azure voting app:
  Includes a front and Back end with Redis
  Using Load Balancer type service
- Link for the code: 

4) Window power shell
Steps to deploy the code:
    az login
    go to the directory where code is stored
    terraform init
    terraform validate
    terraform plan 
    terraform apply 
    az aks get-credintials --resourcegroup aks --name aks-clusterp
    kubectl apply -f azure-vote.yaml
        2 services and 2 deployments
    Kubectl get services
        check the external ip adress to check the app
    
5) Prometheus and grafana
Steps followed in the link were used
Links used: https://www.coachdevops.com/2022/05/how-to-setup-monitoring-on-kubernetes.html
Unable to intall Kube-prometheus-stack
 # helm install stable prometheus-community/kube-prometheus-stack -n prometheus (Stuck here)