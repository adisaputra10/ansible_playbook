# How to work
Install vagrant and virtualbox


# ansible
git clone https://github.com/adisaputra10/ansible_playbook .
vagrant up && vagrant ssh 
cd /vagrant && pip install -r requirement.txt
ansible-playbook -i hosts server.yml 


# ansible with key and password
ansible-playbook -i hosts server.yml -c ssh --ask-pass


# login postgres
psql -h 127.0.0.1 -d acme -U test
