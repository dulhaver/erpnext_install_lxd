## install erpnext in a lxc container

### on your lxd host

1. `lxc launch ubuntu:16.04 erpnext`
2. `lxc exec erpnext -- /bin bash`

### inside the container

1. `apt update`
2. `apt upgrade -y`
3. `apt install -y python-minimal`
4. `su - ubuntu`
5. `wget https://raw.githubusercontent.com/frappe/bench/master/playbooks/install.py`
6. `sudo chmod 774 install.py`
7. `sudo python install.py --production`
