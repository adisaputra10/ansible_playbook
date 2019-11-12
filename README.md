# How to work
* copy folder at roles base on pack
* copy yml file at root base on pack
* add public key ssh at folder, change roles/<name_pack>/templates/authorized_keys
* send public key, setup owner and group roles/<name_pack>/templates/main.yml
* create new user . change roles/<name_pack>/templates/run.sh
* send user name and password with hash, change  roles/<name_pack>/templates/shadow


# ansible
ansible-playbook -i hosts ubuntu-pci.yml ß


# ansible with key and password
ansible-playbook -i hosts ubuntu-pci.yml -c ssh --ask-pass

# Setting SSH
* file ansible : roles/ubuntu/templates/sshd_config
* file ansible : roles/aws/templates/sshd_config
* set private key + password except aws ami
* set idle time ssh 15 menit
* set banner login ssh


# Setting Public Key User
* file ansible : roles/ubuntu/templates/authorized_keys
* file ansible : roles/aws/templates/authorized_keys
* set public key 

# Setting Expired Password
* file ansible : roles/ubuntu/templates/login.defs
* file ansible : roles/aws/templates/login.defs
* set expired password 90 day

# Setting rule password
* file ansible : roles/ubuntu/templates/common-password
* file ansible : roles/aws/templates/system-auth
* uppercase,lowercase,numeric, alpha non-numeric,4 old not same previously

# Setting rule max login ssh and block
* file ansible : roles/ubuntu/templates/common-auth
* file ansible : roles/aws/templates/password-auth
* max 6 failed login, akun will block 30 menit

# Setting ntp client
* file ansible : roles/ubuntu/templates/ntp.conf
* file ansib and le : roles/aws/templates/ntp.conf
* Setting NTP client

# Setting clamav client
* file ansible : roles/ubuntu/templates/clamd.conf
* file ansib and le : roles/aws/templates/clamd.conf
* Setting Clamav client



# Setting Cron Clamav(Auto Scanning)
* file ansible : roles/ubuntu/templates/cron
* file ansib and le : roles/aws/templates//cron
* Setting Cron 


# Setting Hak akses Sudo 
* file ansible : roles/ubuntu/templates/sudoer
* file ansib and le : roles/aws/templates/sudoer
* Setting user can do sudo or not


# Setting Hostname server
* file ansible : roles/ubuntu/templates/hostname
* file ansib and le : roles/aws/templates/hostname
* Setting hostname at server


# Setting Ossec Client
* file ansible : roles/ubuntu/templates/ossec.conf
* file ansib and le : roles/aws/templates/ossec.conf
* Setting ossec client at server













