# Terraform
​
1. What is infrastructure as code (IaC) and why is it important in modern IT operations? What are the advantages?

1.a. IaC uses code, commands written in a machine-readable form, as a substitute for configuring hardware; essentially the infrastructure is managed through code instead of physically/manually.  
The advantages of IaC include
* reliable
* consistent configuration and documentation 
* repeatable, high automation potential
* secure
* faster to deploy
​
2. Explain the concept of "Infrastructure as Code" (IaC) and how Terraform fits into this concept.

2.a. IaC means we can build and manage our infrastructure through configuration files that can in turn be modified (creating versions), reused and shared. The processes of configuration are repetitive and easy to oversee. 

Terraform is a tool that uses declarative code to allow the user to define resources and manage any created infrastructure with the help of human-readable configuration files. Terraform can also track the state of the resources through deployment. 

​
3. What problems do modules help address, and how do they promote reusability?

3.a. Modules in Terraform are files that contain standard code. One module might be a collection of template files for a particular resource, which means it is reusable and helps save time deploying infrastructure. 
​
4. Explain in your own words what the following commands achieve;
​
- `terraform init`
Initializes the directory that contains Terraform config files, starts up Terraform.
​
- `terraform plan`
Shows a preview of what would happen if the apply command is run, without executing anything yet. 
​
- `terraform apply`
Executes the terraform code written to create resources in the config file. 
​
- `terraform destroy`
Tears down any infrastructure that had been created with Terraform. Uses an order of availability, e.g.more primitive resources first 
​
- `terraform fmt`
= terraform format; 
Gives any code written in the configuration file a shape that corresponds to terraform rules, conventions and style("canonical"). Makes adjustments to make code more readable. 
​
- `terraform output`
Fetches the value of an output variable. Output declarations are mostly in a separate file called outputs.tf. I.e to see the ID of a VPC, a block of outputs needs to be added to the configuration. 
​
- `terraform taint`
! Be careful using this command ! Not suggested. 
command "terraform taint 'object_name'" tells Terraform that the named resource is somehow damaged/broken/unsafe to use. Can apply to a resource or security group or other, and means it has to be replaced. 