# DeployMultiArchImagesEKS

## : Execute Terraform Commands
```t
# Change Directory 
cd 04-ingress-basics-terraform-manifests

# Terraform Initialize
terraform init

# Terraform Validate
terraform validate

# Terraform Plan
terraform plan

# Terraform Apply
terraform apply -auto-approve
```

## : Verify Ingress Service
```t
# Verify k8s Deployment and Pods
kubectl get deploy
kubectl get pods

# Verify Ingress (Make a note of Address field)
kubectl get ingress
Obsevation: 
1. Verify the ADDRESS value, we should see something like "ingress-basics-1334515506.us-east-1.elb.amazonaws.com"

# List Services
kubectl get svc

# Verify Application Load Balancer using 
Goto AWS Mgmt Console -> Services -> EC2 -> Load Balancers
1. Verify Listeners and Rules inside a listener
2. Verify Target Groups

# Access App using Browser
kubectl get ingress
http://<ALB-DNS-URL>
or
http://<INGRESS-ADDRESS-FIELD>

# Sample from my environment (for reference only)
http://ingress-basics-154912460.us-east-1.elb.amazonaws.com
```
