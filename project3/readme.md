This project is used to create a t2 micro ec2 instance in aws

Prereq: 
1 pip install boto3  
2 amazon.aws collection : 
    § "ansible-galaxy collection install amazon.aws"
3 create a vault to store the aws IAM user creds to access the AWS
    § store pass in a file: 
        □ openssl rand -base64 2048 > ~/.vault_pass.txt
        
    § pass it to vault and add the access key and secret key: 
        □ ansible-vault create group_vars/secret.yaml --vault-password-file ~/vault_pass.txt
4 to edit the vault file use : 
    § ansible-vault edit group_vars/secret.yaml --vault-password-file ~/vault_pass.txt


To run this playbook use:
    ansible-playbook create-ec2-playbook.yaml --vault-password-file ~/vault_pass.txt

