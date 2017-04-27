# データベースをダンプする
* `mysqldump`コマンドでダンプする。`-B (テーブル名)` で複数データベースをダンプすることができる  
`mysqldump -u xxxx -p -B database_name1 [database_name2 ...] > filename`

# ダンプデータをリストアする
`mysql -u xxxx -p < dumpfile.sql`
