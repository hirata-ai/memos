# ユーザーを削除する
* まずroot でmysql にアクセスする  
`delete from mysql.user where user='(ユーザー名)';`
でユーザー削除できる
* 権限も削除

参考：http://sasuke.main.jp/useri.html#4
