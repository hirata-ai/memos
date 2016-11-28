# mongodb のデータベースの名前を変更する
```
> db.copyDatabase('old_name', 'new_name');
> use old_name
> db.dropDatabase();
```
