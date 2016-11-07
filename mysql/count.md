# mysqlでカウントする
`SELECT * FROM (DB名).(テーブル名)`   
みたいなSELECT文があったとすると，  
`SELECT COUNT(*) FROM (DB名).(テーブル名)`  
で行数をカウントする．


`SELECT COUNT(name) FROM (DB名).(テーブル名)`  
とするとnameカラムでグループ化をして，NULL以外の行数を取得するらしい


もちろんWHERE文で条件を付けるとそれにマッチしただけの行数をカウントしてくれる
