# mongodb のレコードをupdateする

`db.[コレクション名].update({条件}, {$set: {更新するドキュメント}})`  
例: `db.xxx.update({_id: ObjectId("xxx")}, {$set: {description: ""}})`
