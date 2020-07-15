# ApigeeSetup
This repo can be used to 
1. Create EC2 instance on AWS
2. Execute Apigee bootstrap on this instance
3. Configure Apigee component on this instance

Pre req
make sure boto and boto3 are installed
sudo pip install boto
sudo pip install boto3

Under home directory edit .boto file and add
[Credentials]
aws_access_key_id = <aws_access_key_id>
aws_secret_access_key = <aws_secret_access_key>

Update variable files with corresponding values at
ApigeeSetup/ec2-provision/vars/main.yml and
ApigeeSetup/deploy-apigee/vars/main.yml

Execute playbook with a command
execute
ansible-playbook provisionApigee.yml --syntax-check
ansible-playbook provisionApigee.yml
