# Pre requisites

sudo apt-get install ansible
sudo yum install ansible

pip install ansible

git clone https://github.com/ansible/ansible.git
setup.py

mkdir ansible

cd ~ansible


cat ansible

~/ansible/hosts
or
/etc/ansible/hosts


	mail.example.com

	[webservers]
	foo.example.com
	bar.example.com

	[webservers]
	www[01:50].example.com

	[dbservers]
	one.example.com
	two.example.com
	three.example.com

	host1.example.local
	host2.example.local
	host3.example.local
	host4.example.local


	[atlanta]
	host1
	host2

	[atlanta:vars]
	ntp_server=ntp.atlanta.example.com
	proxy=proxy.atlanta.example.com

# /etc/ansible/group_vars/raleigh

---
ntp_server: acme.example.org
database_server: storage.example.org



mkdir -p ~/ansible/files
ssh-keygen -t rsa -f ~/ansible/files/authorized_keys.myuser


ansible-playbook playbook.yml -i ./hosts

mkdir ansible-apache
