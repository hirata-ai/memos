# Docker をインストールする
※centos7 系
* `/etc/yum.repos.d/docker.repo` に以下を書き込む
```
name=Docker Repository
baseurl=https://yum.dockerproject.org/repo/main/centos/7
enabled=1
gpgcheck=1
gpgkey=https://yum.dockerproject.org/gpg
```
* `(sudo) yum -y install docker-engine` でDocker をインストール
* Docker サービスをスタート  
```
(sudo) systemctl start docker
(sudo) systemctl enable docker
```
