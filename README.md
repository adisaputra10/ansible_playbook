# How to work
Install vagrant and virtualbox


# ansible
git clone https://github.com/adisaputra10/ansible_playbook . <br>
vagrant up && vagrant ssh <br>
sudo add-apt-repository ppa:ansible/ansible-2.5 </br>
sudo apt-get update  && apt install ansible</br>
cd /vagrant && pip install -r requirement.txt <br>
ansible-playbook -i hosts server.yml -e env=ubuntu<br>


# ansible with key and password
ansible-playbook -i hosts server.yml -e env=ubuntu -c ssh --ask-pass


# login postgres
psql -h 127.0.0.1 -d acme -U test
# add label kubernetes
kubectl lable node nama_node node-role.kubernetes.io/infra="true" --overwrite
