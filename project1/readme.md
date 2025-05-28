This playbook will install httpd server on all the servers and copy the html file

running the playbook:

ansible-playbook -i inventory.ini run_playbook.yaml

before running check below is working or not:

ansible -i inventory -u ec2-user -m ping all

