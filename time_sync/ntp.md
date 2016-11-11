# 時刻同期する(cenos6より前のバージョン)
NTPで時刻同期をする(centos7以降だと`Chrony`というものになってるらしい)  
* とりあえずntpをインストール  
`(sudo) yum -y install ntp`  
* ntpdを起動  
`service ntpd start`

* 同期先サーバの設定などは`/etc/ntp.conf`を編集．  
```diff
-server 0.centos.pool.ntp.org iburst
-server 1.centos.pool.ntp.org iburst
-server 2.centos.pool.ntp.org iburst
-server 3.centos.pool.ntp.org iburst
+server ntp.nict.jp
+server ntp.jst.mfeed.ad.jp
```
NICTがNTPサーバを提供してるらしい．他にはプロバイダのNTPサーバとか指定するらしい．

* 設定変えたら設定ファイルを再読み込み  
`service ntpd reload`

* 同期先サーバと同期してるかどうかの確認  
`ntpq -p`  
上のコマンド叩くと
```
remote           refid      st t when poll reach   delay   offset  jitter
==============================================================================
*ntp-b2.nict.go. .NICT.           1 u   38   64  377    6.158    0.358   0.385
+ntp2.jst.mfeed. 133.243.236.17   2 u   37   64  377    8.586    2.721   0.339
```
こんな感じのが表示される．* とか + がつけば同期してるらしい．

* 再起動した時にntpdを再起動するようにする  
`chkconfig ntpd on`  
これでサーバ再起動時でも自動でntpdが起動する．  
ちなみに`chkconfig --list ntpd` して  
```
ntpd            0:off   1:off   2:on    3:on    4:on    5:on    6:off
```
こんな感じになってればちゃんと設定されている．

参考：
http://qiita.com/megu_ma/items/bb902740ee7de9ddd102
