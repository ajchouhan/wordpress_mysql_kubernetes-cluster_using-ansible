# wordpress_mysql_kubernetes-cluster_using-ansible
Wordpress Mysql Over Kubernetes Setup Role
Hi Guys
I have created this repository to setup wordpress-mysql setup over kubernetes multi-node cluster cluster over aws in a few minutes.
So, use this role. This is created for educational and learning purpose. You can find roles at ansible-galaxy also.
Folloing things you have to provide in awsrole to launch an instance:--

key_name: "{{ ssh_key }}"            #you have to provide your key Ex. aj  ( but before provide you key change its permision Ex. chmod 400 aj )   
instance_type: "{{ i_type }}"        #you have to provide instance type Ex. t2.micro
image: "{{ ami }}"                   #you have to provide ami Ex.ami-0f5a36d8151016a65
region: "{{ region }}"               #you have to provide region name Ex. ap-south-1b
group_id: "{{ sg_groups }}"          #you have to security group name
count: "{{ count_ins }}"   
instance_tags:
       Name: "{{ tag_name }}"        #instance name
vpc_subnet_id: "{{ subnet_id }}"     #you have to provide subnet_id 
aws_access_key: "{{ access_key }}"   #you have provide access_key
aws_secret_key: "{{ secret_key }}"   #you have to provide secret_key

TO RUN MAIN PLAYBOOK: ansible-playbook main.yml -b
