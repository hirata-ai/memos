# vsftpについて
## 概要
vsftpは一般的なFTPサーバのこと．  
インストール方法とかは忘れたので割愛．(yumで入れた気がする)

## 設定
* 設定ファイルは通常は`/etc/vsftpd/vsftpd.conf` にある．
* FTP利用できるユーザを登録するには`/etc/vsftpd/vsftpd.conf` に
```
userlist_enable=YES
userlist_deny=NO
```
を追記し，`/etc/vsftpd/user_list` にFTP接続したいユーザ名を追記する．
