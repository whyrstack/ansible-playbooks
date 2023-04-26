## Playbook installs necessary components of a functioning kubeadm cluster <br>

### Required: <br>
**2** EC2 Instances min 4GB RAM and 2 CPU <br>

### 1. Provision both EC2 Instances <br>
On both EC2 perform the following steps <br>

### 2. Copy over repository to your local machine
```
$ git clone https://xxx
```
### 3. Put privateIP in the local inventory file <br>

### 4. On your local machine generate rsa key to be used for ssh <br>
```
$ ssh-keygen -t rsa
$ cat ~/.ssh/id_rsa.pub
```

### 5. SSH to ec2 instance and add public key to authorized_keys <br>
```
$ echo "<id_rsa.pub output>" >> ~/.ssh/authorized keys
```

### 6. Test if ansible connection is working towards EC2 instances <br>
```
$ ansible all -m ping <br>
$ ansible all -m ansible.builtin.command -a "hostnamectl"
```
