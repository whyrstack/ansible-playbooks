## Playbook installs necessary components of a functioning kubeadm cluster <br>

### Required: <br>
**2** EC2 Instances min 4GB RAM and 2 CPU <br>

### Provision both EC2 Instances <br>
On both EC2 perform the following steps <br>

### Copy over repository <br>
Put privateIP in the inventory file <br>

### On your local machine <br>
```
$ ssh-keygen -t rsa # generate RSA key <br>
$ cat ~/.ssh/id_rsa.pub <br>
```

### SSH to ec2 instance <br>
```
$ echo "<id_rsa.pub output>" >> ~/.ssh/authorized keys <br>
```

### Test connectivity <br>
```
$ ansible all -m ping <br>
$ ansible all -m ansible.builtin.command -a "hostnamectl" <br>
```
