# QUESTION 7

Which of the following sequences describes the Terraform workflow for: 
1) Downloading plugins and setting up backend,
2) Generating and executing changes,
3) Removing all resources? (1 point)

a. terraform import, terraform apply -y, terraform destroy <br>
b. teraform init, terraform plan -auto-apply, terraform rm <br>
c. terraform init, terraform run -auto-approve, terraform destroy <br>
d. terraform init, terraform apply -auto-approve, terraform destroy <br>
e. terraform import, terraform apply -y, terraform rm <br>

### ANSWER

1) download and setup need "init" statement
2) Generating and executing need "apply" statement.  By default, apply asks for a manual "yes" confirmation. The auto-approve has a function to skip that confirmation prompt and made the execution quicker
3) Removing resource need "destroy" statement
   
so, the answer is (d) : terraform init, terraform apply -auto-approve, terraform destroy
