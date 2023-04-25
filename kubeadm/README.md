# Follow
Put IP in the inventory file <br>
$ ssh-keygen -t rsa # generate RSA key <br>
$ cat ~/.ssh/id_rsa.pub <br>
SSH to ec2 instance <br>
$ echo "<id_rsa.pub output>" >> ~/.ssh/authorized keys <br>

# Test connectivity <br>
$ ansible all -m ping <br>
$ ansible all -m ansible.builtin.command -a "hostnamectl" <br>
