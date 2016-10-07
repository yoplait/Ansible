# Ansible
# Pre requisites

#
# Instlal
#

# Cygwin

apt-get install gcc

apt-get install python-crypto
apt-get install python-openssl
apt-get install python-setuptools
apt-get install git (2.5.x)
apt-get install nano
apt-get install openssh
apt-get install openssl
apt-get install openssl-devel
apt-get install build-essential libssl-dev libffi-dev python-dev

apt-get install python-dev 
apt-get install libffi-dev
apt-get install libssl-dev
apt-get install python-cffi
apt-get install libffi-devel

pip install --upgrade cffi
pip install paramiko 
pip install PyYAML 
pip install Jinja2 
pip install httplib2 
pip install six 
pip install markupsafe  
pip install docker-py
pip install ansible==2.0.2.0

pip install cryptography
pip install --upgrade --force-reinstall pip virtualenv

pip install ansible

curl -O https://pypi.python.org/packages/source/P/PyYAML/PyYAML-3.10.tar.gz
curl -O https://pypi.python.org/packages/source/J/Jinja2/Jinja2-2.8.tar.gz

tar -zxvf Jinja2-2.8.tar.gz
tar -zxvf PyYAML-3.10.tar.gz

cd Jinja2-2.8
python setup.py install
cd ..
cd PyYAML-3.10
python setup.py install

# sshpass
curl -O -L http://downloads.sourceforge.net/project/sshpass/sshpass/1.05/sshpass-1.05.tar.gz
tar xvzf sshpass-1.05.tar.gz
cd sshpass-1.05
./configure
make
make install

# ubuntu

sudo apt-add-repository -y ppa:ansible/ansible
sudo apt-get update
sudo apt-get install -y ansible

# centos

sudo rpm -iUvh http://dl.fedoraproject.org/pub/epel/7/x86_64/e/epel-release-7-5.noarch.rpm
sudo yum -y update

sudo yum -y install python
sudo yum -y install ansible

pip install ansible-playbook

git clone https://github.com/ansible/ansible.git
setup.py

# verify version 

ansible --version

# Inventory file

sudo mkdir /etc/ansible
sudo touch /etc/ansible/hosts

sudo cp /etc/ansible/hosts /etc/ansible/hosts.old
sudo mv /etc/ansible/hosts /etc/ansible/hosts.orig

sudo nano /etc/ansible/hosts

eu-fcpp-a004 ansible_ssh_pass='!t4yc1Bw9DKQSf!t' ansible_ssh_user=perezjc ansible_user=perezjc
eu-fcpp-a004

[CI-JENKINS]
eu-fcpp-a001 ansible_ssh_user=perezjc ansible_sudo_pass='!t4yc1Bw9DKQSf!t' ansible_ssh_pass='!t4yc1Bw9DKQSf!t' 
eu-fcpp-a002 ansible_ssh_user=perezjc ansible_sudo_pass='!t4yc1Bw9DKQSf!t' ansible_ssh_pass='!t4yc1Bw9DKQSf!t' 
eu-fcpp-a003 ansible_ssh_user=perezjc ansible_sudo_pass='!t4yc1Bw9DKQSf!t' ansible_ssh_pass='!t4yc1Bw9DKQSf!t' 
eu-fcpp-a004 ansible_ssh_user=perezjc ansible_sudo_pass='!t4yc1Bw9DKQSf!t' ansible_ssh_pass='!t4yc1Bw9DKQSf!t' 
eu-fcpp-a005 ansible_ssh_user=perezjc ansible_sudo_pass='!t4yc1Bw9DKQSf!t' ansible_ssh_pass='!t4yc1Bw9DKQSf!t' 

eu-fcpp-a004 ansible_user=perezjc ansible_ssh_pass='!t4yc1Bw9DKQSf!t' ansible_sudo_pass='!t4yc1Bw9DKQSf!t'
eu-fcpp-a001 ansible_user=perezjc ansible_ssh_pass='!t4yc1Bw9DKQSf!t' ansible_sudo_pass='!t4yc1Bw9DKQSf!t'
eu-fcpp-a002 ansible_user=perezjc ansible_ssh_pass='!t4yc1Bw9DKQSf!t' ansible_sudo_pass='!t4yc1Bw9DKQSf!t'
eu-fcpp-a003 ansible_user=perezjc ansible_ssh_pass='!t4yc1Bw9DKQSf!t' ansible_sudo_pass='!t4yc1Bw9DKQSf!t'
eu-fcpp-a005 ansible_user=perezjc ansible_ssh_pass='!t4yc1Bw9DKQSf!t' ansible_sudo_pass='!t4yc1Bw9DKQSf!t'

[CI-SELENIUM]
eu-fcpp-a006 ansible_user=perezjc ansible_ssh_pass='!t4yc1Bw9DKQSf!t' ansible_sudo_pass='!t4yc1Bw9DKQSf!t'
eu-fcpp-a007 ansible_user=perezjc ansible_ssh_pass='!t4yc1Bw9DKQSf!t' ansible_sudo_pass='!t4yc1Bw9DKQSf!t'
eu-fcpp-a008 ansible_user=perezjc ansible_ssh_pass='!t4yc1Bw9DKQSf!t' ansible_sudo_pass='!t4yc1Bw9DKQSf!t'
eu-fcpp-a009 ansible_user=perezjc ansible_ssh_pass='!t4yc1Bw9DKQSf!t' ansible_sudo_pass='!t4yc1Bw9DKQSf!t'

[CI-BUILDS]
eu-fcpp-b001 ansible_user=perezjc ansible_ssh_pass='!t4yc1Bw9DKQSf!t' ansible_sudo_pass='!t4yc1Bw9DKQSf!t'
eu-fcpp-b002 ansible_user=perezjc ansible_ssh_pass='!t4yc1Bw9DKQSf!t' ansible_sudo_pass='!t4yc1Bw9DKQSf!t'
eu-fcpp-b003 ansible_user=perezjc ansible_ssh_pass='!t4yc1Bw9DKQSf!t' ansible_sudo_pass='!t4yc1Bw9DKQSf!t'
eu-fcpp-b004 ansible_user=perezjc ansible_ssh_pass='!t4yc1Bw9DKQSf!t' ansible_sudo_pass='!t4yc1Bw9DKQSf!t'
eu-fcpp-b005 ansible_user=perezjc ansible_ssh_pass='!t4yc1Bw9DKQSf!t' ansible_sudo_pass='!t4yc1Bw9DKQSf!t'
eu-fcpp-b006 ansible_user=perezjc ansible_ssh_pass='!t4yc1Bw9DKQSf!t' ansible_sudo_pass='!t4yc1Bw9DKQSf!t'
eu-fcpp-b007 ansible_user=perezjc ansible_ssh_pass='!t4yc1Bw9DKQSf!t' ansible_sudo_pass='!t4yc1Bw9DKQSf!t'
eu-fcpp-b008 ansible_user=perezjc ansible_ssh_pass='!t4yc1Bw9DKQSf!t' ansible_sudo_pass='!t4yc1Bw9DKQSf!t'
eu-fcpp-b009 ansible_user=perezjc ansible_ssh_pass='!t4yc1Bw9DKQSf!t' ansible_sudo_pass='!t4yc1Bw9DKQSf!t'
eu-fcpp-b010 ansible_user=perezjc ansible_ssh_pass='!t4yc1Bw9DKQSf!t' ansible_sudo_pass='!t4yc1Bw9DKQSf!t'


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

# ssh keys Creating pub SSH keys

ssh-keygen -N '' -f /root/.ssh/id_rsa
ssh-keygen -t rsa -C "perezpardojc@gmail.com"

# Coping local key to other.server.net

shell cat /tmp/id_rsa.tmp | ssh -p 2244 root@other.server.net "cat >> /root/.ssh/authorized_keys"
ssh-copy-id user@child1.dev
ssh-copy-id vagrant@192.168.32.61

cp /vagrant/keys/id_rsa.pub /home/vagrant/.ssh/id_rsa.tmp
sudo cat /home/vagrant/.ssh/id_rsa.tmp >> /home/vagrant/.ssh/authorized_keys

# user special

cat ~/.ssh/config
nano ~/.ssh/config

Host *
    HostName *
    User perezjc


Host X01
    HostName eu*

Host X02
    HostName am*


Host X01 X02 ...
     User perezjc



nano /etc/ansible/ansible.cfg

ask_sudo_pass=True
ask_vault_pass=True
inventory = /etc/ansible/hosts
log_path=/var/log/ansible.log
remote_user = perezjc
sudo_exe=sudo
sudo_user=root
become=True
become_user=root


# test ansible

ansible: error: 
Sudo arguments ('--sudo', '--sudo-user', and '--ask-sudo-pass') and su arguments ('-su', '--su-user', and '--ask-su-pass') and 
become arguments ('--become', '--become-user', and '--ask-become-pass') are exclusive of each other

ansible test -a "/usr/bin/foo"
ansible test -a "/usr/bin/foo" -u perezjc

ping eu-fcpp-a004
ssh eu-fcpp-a004
ssh perezjc@eu-fcpp-a004

!t4yc1Bw9DKQSf!t


sudo -u root sudo echo "success"

#running

export ANSIBLE_HOST_KEY_CHECKING=False

ansible eu-fcpp-a004 -m ping -vvvv
ansible eu-fcpp-a004 -m ping -vvvv -s 
ansible eu-fcpp-a004 -m ping -vvvv --ask-become-pass
ansible eu-fcpp-a004 -m shell -a 'cat /etc/shadow' -vvvv -s --ask-sudo-pass
ansible eu-fcpp-a004 -m shell -a 'cat /etc/shadow' -vvvv -s

ansible eu-fcpp-a004 -m ping -vvvv --become --become-user --become-method --ask-become-pass  

ansible eu-fcpp-a004 -m ping -v --become-user root --ask-become-pass
ansible eu-fcpp-a004 -m ping -u perezjc -s -k
ansible eu-fcpp-a004 -m ping -vvvvv

ansible eu-fcpp-a004 -m ping -u perezjc -b
ansible eu-fcpp-a004 -m ping -u perezjc -b --become-user root
ansible eu-fcpp-a004 -m ping -u perezjc -b --become-user root -v
ansible eu-fcpp-a004 -m ping -u perezjc -b --become-user root -vvvvvv -K

ansible eu-fcpp-a004 -m ping -vvv -s -k -u perezjc
ansible eu-fcpp-a004 -m ping -vvvv -s -k -u perezjc

ansible eu-fcpp-a004 -m shell -a 'ls /' -vvv -s -k -u perezjc

ansible all -m ping
ansible all -m ping -s -k -u vagrant
ansible all -m ping -s -k -u vagrant -vvv

ansible CI-JENKINS -i tests -m ping
ansible CI-JENKINS -m ping -k

ansible CI-JENKINS -m ping -u perezjc --ask-pass
ansible CI-SELENIUM -m ping -u perezjc
ansible CI-BUILDS -m ping -u perezjc

ansible CI-JENKINS -a "free -m" -u perezjc


ansible all -m shell -a 'ls /'
ansible eu-fcpp-a004 -m shell -a 'ls /'

ansible all -s -m shell -a 'sudo apt-get -y install nginx'

ansible all -m shell -a 'cat /etc/shadow'
ansible eu-fcpp-a004 -m shell -a 'cat /etc/shadow'



ansible all -s -m shell -a 'sudo yum -y install epel-release'
ansible all -s -m shell -a 'sudo yum -y install nginx'
ansible all -s -m shell -a 'sudo systemctl start nginx'

sudo firewall-cmd --permanent --zone=public --add-service=http 
sudo firewall-cmd --permanent --zone=public --add-service=https
sudo firewall-cmd --reload


ansible all -s -m apt -a 'pkg=nginx state=installed update_cache=true'
ansible all -s -m yum -a 'pkg=nginx state=installed update_cache=true'


# run playbook

ansible-playbook -s -k -u vagrant nginx.yml
ansible-playbook -s nginx.yml
ansible-playbook -s -k -u vagrant nginx.yml

!t4yc1Bw9DKQSf!t

ansible eu-fcpp-a004 -m ping -vvvv --ask-become-pass
ansible eu-fcpp-b006 -m shell -a 'cat /etc/shadow' -vvvv -s

ansible eu-fcpp-b004 -a /bin/date -vvvv -s #no funciona
ansible eu-fcpp-b004 -a /bin/date -vvvv --ask-become-pass#no funciona


eu-fcpp-b004 ansible_ssh_pass=!t4yc1Bw9DKQSf!t ansible_ssh_user=perezjc


ansible eu-fcpp-b001 -a /bin/date -vvvvv
ansible eu-fcpp-b001 -a /bin/date -vvvvv --ask-become-pass

ansible eu-fcpp-b001 -a /usr/bin/whoami -vvvvv
ansible eu-fcpp-b001 -a /usr/bin/whoami -vvvvv --ask-become-pass

ansible CI-BUILDS -a /bin/date -vvvvv
ansible CI-BUILDS -m ping -vvvvv

# dry-run

ansible-playbook playbook.yml -u someuser -i hosts --sudo --vault-password-file=vault.txt 

ansible-playbook -C ansible/test1.yml --ask-become-pass
ansible-playbook -C ansible/test1.yml

ansible eu-fcpp-b006 -M ansible/test.yml -vvvv 

ansible-playbook -C ansible/test1.yml --ask-become-pass -vvvvvv
ansible-playbook -C ansible/user/ansible.yml -vvvvvv



ansible eu-fcpp-b001 -a /bin/date -vvvvv

ansible-playbook ansible/test/test.yml -vvvvvvv --ask-become-pass
!t4yc1Bw9DKQSf!t

ansible-playbook ansible/user/ansible.yml -vvvvvvv 
ansible-playbook ansible/user/ansible.yml -vvvvvvv --ask-become-pass
!t4yc1Bw9DKQSf!t

ansible-playbook ansible/user/ansible_key.yml -vvvvvvv --ask-become-pass

ansible eu-fcpp-b001 -a /bin/date -vvvvv
ansible eu-fcpp-b001 -a /bin/date -vvvvv --ask-become-pass


ssh-keygen -t rsa -C "ansible@iconplc.com"
tomatesOM6M98!f71568999fdsafdasa

ssh -i /home/PerezJu/.ssh/id_rsa ansible@eu-fcpp-b001

ssh ansible@eu-fcpp-b001

ansible eu-fcpp-b001 -m ping -vvvv
ansible eu-fcpp-b004 -m ping -vvvvv

ansible CI-BUILDS -m ping -vvvvvv
ansible CI-BUILDS-TEST -m ping -vvvvvv

	
ansible eu-fcpp-b001 -m ping -vvvvv --ask-become-pass
ansible eu-fcpp-b002 -m ping -vvvvv --ask-become-pass

ssh -i /home/ansible/.ssh/id_rsa ansible@eu-fcpp-b001

!t4yc1Bw9DKQSf!t
tomatesOM6M98!f71568999fdsafdasa


ansible all -m command --args "uptime"

ansible-playbook all ansible/installs/installs.yml -vvvvvvv --ask-become-pass

ansible-playbook [CI-BUILDS-TEST] ansible/installs/files.yml -vvvvvvv --ask-become-pass
ansible-playbook ansible/files/files.yml CI-BUILDS-TEST -vvvvvvv --ask-become-pass --list-hosts
ansible-playbook ansible/files/files.yml -vvvvvvv --ask-become-pass --list-hosts

ansible-playbook ansible/files/files.yml --extra-vars "target=eu-fcpp-b001" --list-hosts
ansible-playbook ansible/files/files.yml --extra-vars "target=CI-BUILDS-TEST" --list-hosts
ansible-playbook ansible/files/files.yml --extra-vars "target=CI-BUILDS" --list-hosts

ansible-playbook ansible/files/files.yml --list-hosts
ansible-playbook ansible/files/files.yml --check

ansible-playbook ansible/files/files.yml --extra-vars "target=eu-fcpp-b001" --ask-become-pass
ansible-playbook ansible/files/files.yml --extra-vars "target=CI-BUILDS" --ask-become-pass

ansible-playbook -i "eu-fcpp-b001," ansible/files/files.yml 

#
# copy from my desktop to server
#

scp -r ansible ansible@eu-fcpp-a002:/home/ansible/
