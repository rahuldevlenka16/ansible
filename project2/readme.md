created roles using:
ansible-galaxy role init httpd-role-demo

tasks folder container task to install httpd, copy the html from files, check the httpd

here in the playbook instead of specifying task in project1, we will specify the role to use

to run playbook: "ansible-playbook -i inventory.ini run-playbook.yaml"

Note:
1. always make sure you can do passwordless auth from the control node, the current system, 
    "ssh-keygen -i rsa"
    "ssh-copy-id -f -o "IdentityFile=ansible-kp.pem" ec2-user@<ip>"
    test with ssh ec2-user@<ip> or ping module
2. enable the ssh port 22 (and port 80 for http access) in the inbound sg of the target ec2 instances
3. make sure correct ec2 instance ip is used in the inventory files