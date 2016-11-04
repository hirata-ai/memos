# Apacheでリダイレクト処理
* Mod_Rewriteを使ってリダイレクトをかける
* `RewriteCond` が条件，そのあとの`RewriteRule` がリダイレクトルールになる．
* `RewriteCond` は正規表現を利用できるので，例外を指定する場合，`!` から始めると例外になる
```
RewriteCond %{HTTPS} off
RewriteCond %{REQUEST_URI} ^.*$
RewriteCond %{REQUEST_URI} !^/image/.*$
RewriteRule ^(.*)$ https://%{HTTP_HOST}%{REQUEST_URI} [R=301,L]
```
上記だと`http://xxxxxxx/image/` 以下がhttpsにリダイレクトかからなくなる(たぶん)
