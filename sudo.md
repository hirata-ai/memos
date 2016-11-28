# sudoers の設定をする
## 特定のユーザでのsudo をパスワードなしにする
* visudo コマンドでsudoers ファイルを編集  
`sudo visudo`
* 末尾に以下を追加  
`<username> ALL=NOPASSWD: ALL`
* vi から抜けたら終わり
