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
