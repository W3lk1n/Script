Install the prerequisites:
```
sudo yum install yum-utils
cd /etc/yum.repos.d/
wget https://raw.githubusercontent.com/W3lk1n/Script/master/Centos7/nginx.repo
```

By default, the repository for stable nginx packages is used. If you would like to use mainline nginx packages, run the following command:
> sudo yum-config-manager --enable nginx-mainline

To install nginx, run the following command:
> sudo yum install nginx

When prompted to accept the GPG key, verify that the fingerprint matches 573B FD6B 3D8F BC64 1079 A6AB ABF5 BD82 7BD9 BF62, and if so, accept it.
