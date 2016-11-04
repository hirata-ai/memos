# sshで利用する鍵を作成する
* `ssh-keygen -t rsa` で秘密鍵(id_rsa)と公開鍵(id_rsa.pub)が作成される．(デフォルトでは`~/.ssh/` 以下に保存される)
* 公開鍵を`authorized_keys` としてコピーなりリネームする．
* authorized_keys のパーミッションを600にする．`sudo chmod 600 authorized_keys`(鍵認証でログインする場合，デフォルトではauthorized_keys を参照しにいくため)
