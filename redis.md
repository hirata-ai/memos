# redis
## redis インストール
centos7系の場合
```
sudo yum install -y epel-release
wget http://rpms.famillecollet.com/enterprise/remi-release-7.rpm
sudo rpm -Uvh remi-release-7*.rpm
sudo yum --enablerepo=remi,remi-test,epel install -y redis
```
## redis 起動
`sudo systemctl start redis`
