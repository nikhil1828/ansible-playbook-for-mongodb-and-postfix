PRE-REQUISITE:

1. An AWS account with required permissions to create an EC2 instance.

2. An EC2 instance with 22 port allowed for installing MongoDB and Postfix.

3. An AWS SES SMTP credentials.


STEPS TO RUN THIS CODE:

1. Modify the "vars/all.yaml" file with your smtp_endpoint, smtp_username and smtp_password with your SMTP credentials and SMTP endpoint and also modify the "roles/postfixsetup/tasks/main.yaml" with your smtp_endpoint at line no 23.

2. Modify the "hosts" file with your EC2 instance's public IP

3. Now run this ansible playbook using ansible command

    ansible-playbook  -i hosts  -u ubuntu -b playbook.yaml --private-key <your ec2 private key path>
