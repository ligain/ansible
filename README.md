
# Ansible  practice
This repository contains a simple `Ansible` playbook to install `nginx` server on the vagrant virtual machine from `Vagrantfile`


# Run  
0) `vagrant` and `Ansible` should be installed on your system
```
$ vagrant -v
Vagrant 2.2.5
$ ansible --version
ansible 2.9.1
...
```
1) Clone this repository
```bash  
$ git clone https://github.com/ligain/ansible.git  
``` 
2) Go to project folder
```bash  
$ cd ansible/
```  
3) Run `Vagrantfile`
```bash  
$ vagrant up
```
4) After the vagrant virtual machine will have been setuped  you can provision it with ansible playbook
```
$ ansible-playbook nginx.yml

PLAY [Install nginx server] ***********************
...
```
5) SSH to the vagrant virtual machine and check that nginx is up and running
```
$ vagrant ssh
Last login: Sun Dec  8 16:12:07 2019 from 10.0.2.2
[vagrant@nginx ~]$ curl localhost:8080
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN" "http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd">

<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en">
    <head>
        <title>Test Page for the Nginx HTTP Server on Red Hat Enterprise Linux</title>
        <meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
        <style type="text/css">
...
``` 

# Project Goals 
The code is written for educational purposes.