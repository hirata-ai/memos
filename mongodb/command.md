# mongodb を操作する
## シェルからmongodb に接続
`mongo`

## mongodb コマンド
* データベース表示  
`show databases`
* データベース選択  
`use [データベース名]`
* コレクション表示  
`show collections`
* コレクション内全件表示  
`db.[コレクション名].find()`
* ソートする場合は後ろに`.sort({sort_key:1})` を付ける(逆順なら-1)  
`db.[コレクション名].find().sort({sort_key:1})`
* find した結果の集計をするときは末尾に`.count()`を付けるだけ  
`db.[コレクション名].find().sort({sort_key:1}).count()`

* 検索フィールドを指定する場合  
`db.[コレクション名].find({}, {(検索フィールド名): 1})`
* 検索条件を指定する場合  
`db.[コレクション名].find({(フィールド名): (検索文字列)})`  
例：`db.users.find({status: "A"})` (statusフィールドが"A"のものだけ表示)
