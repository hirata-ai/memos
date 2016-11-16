# 時刻同期する(cenos7~)
Chrony で時刻同期をする(centos7から。それより前はntp で時刻同期する)  
(ntp でも時刻同期はできる)   
chrony の方が優れてるらしいので特に理由がなければchrony にした方がよさそう．([参考](https://access.redhat.com/documentation/ja-JP/Red_Hat_Enterprise_Linux/7/html/System_Administrators_Guide/ch-Configuring_NTP_Using_the_chrony_Suite.html#sect-differences_between_ntpd_and_chronyd))  
説明はだいたい[ntp.md](ntp.md) と同じ．
* とりあえずchrony をインストール  
`(sudo) yum install chrony`
* chrony 起動  
`(sudo) systemctl start chronyd`

* 同期先サーバの設定などは`/etc/ntp.conf`を編集．  
```diff
-server 0.centos.pool.ntp.org iburst
-server 1.centos.pool.ntp.org iburst
-server 2.centos.pool.ntp.org iburst
-server 3.centos.pool.ntp.org iburst
+server ntp.nict.jp iburst
+server ntp.jst.mfeed.ad.jp iburst
```
iburst を付けると初回同期にかかる時間が改善されるらしい．  
ntp の時と同様にnict のサーバにする．  
jst のサーバはnict のサーバと同期したサーバ．

* 設定変えたらchronyd を再起動  
`(sudo) systemctl restart chronyd`

* 同期しているかどうかを確認する  
`chronyc tracking`  

参考：
https://access.redhat.com/documentation/ja-JP/Red_Hat_Enterprise_Linux/7/html/System_Administrators_Guide/ch-Configuring_NTP_Using_the_chrony_Suite.html
