Create a directory in VS code
mkdir Ec2-Vpc  
cd Ec2-Vpc
create all the tf files in this folder
Create a terraform work space like example
terraform workspace new rajesh1
After this it will creates a terraform.tfstate.d file in EC2-Vpc folder
cd terraform.tfstate.d
You will see waht ever the workspace you created like rajesh1
cd ..
terraform workspace select rajesh1
terraform init
terraform plan -var-file="terraform-rajesh1.tfvars"
terraform apply -var-file="terraform-rajesh1.tfvars"

NOTE:
If we want to create workspace with the name rajesh1 and create resources in that worksapce then
Then the name of the tfvars file (terraform.tfvars) should be like this terraform-rajesh1.tfvars

If we do not create any workspace useing default workspace
Then the name of the tfvars file should be like this terraform.tfvars
