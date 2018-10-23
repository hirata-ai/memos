# timezoneを設定する(CentOS6)
* 現在設定されているtimezoneを確認するときは，`date` コマンドで確認する。
```
[vagrant@localhost ~]$ date
Mon May 22 06:41:33 UTC 2017
```
* タイムゾーンの設定は`/etc/localtime` で設定してある．  
* 変更する場合は，`/usr/share/zoneinfo` 以下にある，自分の設定したいタイムゾーンのファイルを`/etc/localtime` にコピーすることで設定できる．
```
# cp -p /etc/localtime /etclocaltime_org
# cp /usr/share/zoneinfo/Japan /etc/localtime
# date
Mon May 22 15:46:03 JST 2017
```
* タイムゾーンを変更した後は`shutdown -r now` などでサーバの再起動をする．（再起動しないとログのタイムゾーンが反映されないため）