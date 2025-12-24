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

In the terraform-rajesh1.tfvars
we have to give what ever the region we seclect that regions
ami id 
instance type
key pair
example like i want create ec2 and vpc in mumbai region ap-south-1 then it should be like this

region         = "ap-south-1"
ami_id         = "ami-02b8269d5e85954ef" 
key_name       = "script" //what ever the keypairs that we created in that region that we have to give here(Go to ec2 dashboard -> click key pairs)
instance_type  = "t3.medium"
server1_volume = 20
server2_volume = 15
server3_volume = 10
server4_volume = 10
