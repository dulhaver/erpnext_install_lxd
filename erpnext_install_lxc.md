# install erpnext in a lcd/lxc container

### on your lxd host

1. `lxc launch ubuntu:16.04 erpnext`
2. `lxc exec erpnext -- /bin bash`


### inside the container

1. `sudo apt update`
2. `sudo apt upgrade -y`
3. `sudo apt install -y python-minimal`
4. `sudo adduser frappe`
5. `su - frappe
6. `wget https://raw.githubusercontent.com/frappe/bench/master/playbooks/install.py`
7. `sudo chmod 774 install.py`
8. `sudo python install.py --production`

