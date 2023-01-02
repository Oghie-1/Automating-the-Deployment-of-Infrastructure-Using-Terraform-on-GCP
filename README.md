# Automating-the-Deployment-of-Infrastructure-Using-Terraform-on-GCP
Terraform is a powerful tool that allows you to automate the deployment and management of infrastructure resources. With Terraform, you can define your infrastructure as code and deploy it using a consistent workflow.  This project provides a simple example of how to use Terraform to deploy a web server on GCP. Terraform configuration with a module to automate the deployment of Google Cloud infrastructure. As your configuration changes, Terraform can create incremental execution plans, which allows you to build your overall configuration step by step.

Much more than that, the instance module allows you to re-use the same resource configuration for multiple resources while providing properties as input variables.  


<h3>Objectives</h3>

<li>Task 1. Set up Terraform and Cloud Shell</li>
<li>Task 2. Create network and its resources</li>
<li>Task 3. Verify your deployment</li>


<h3>Prerequisites<h3>

<li>Terraform</li>
<li>GCP Account</li>

<h3>Setup<h3>

```
git clone https://github.com/USERNAME/terraform-gcp-infrastructure-automation.git
cd terraform-gcp-infrastructure-automation

```
<p>Create a service account and download the private key file:
  <ul>
  <li>Navigate to the IAM & Admin page in the GCP console.</li>
  <li>Click the Create service account button.</li>
  <li> Enter a name and description for the service account.</li>
  <li>Click the Create button.</li>
  <li>Click the Create key button and download the private key file.</li>
  <li>Create an .env file and add the path to the private key file:</li>
    <ul>
 </p>
 
``` 
touch .env 
GOOGLE_APPLICATION_CREDENTIALS=path/to/private/key/file.json
```

<li>Initialize your working directory:</li>

```
terraform --version
terraform init

#Create auto mode network along with its firewall rule inside the mynetwork.tf

# Define  VM instances by creating a VM instance module.

mkdir instance
cd instance

#Populate your main.tf file with the resource of your choice

vim main.tf

#To rewrite the Terraform configuration files to a canonical format and style, run the following command:

terraform fmt

#Initialize Terraform, run the following command:
terraform init

```
<li>Create an execution plan:</li>

```
terraform plan

```
<li>Deploy the infrastructure:</li>

```
terraform apply

#To confirm the planned actions, type:

yes

```

<li><p>Usage
  To view the web server, navigate to the public IP address of the GCE instance in your web browser.
</p></li>

<li><p>Cleanup
  To destroy the infrastructure, run the following command:
</p></li>

```
terraform destroy

```





    
   
    
    
