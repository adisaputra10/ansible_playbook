# How to work



# ansible
ansible-playbook -i hosts server.yml 


# ansible with key and password
ansible-playbook -i hosts server.yml -c ssh --ask-pass


# login postgres
psql -h 127.0.0.1 -d acme -U test
