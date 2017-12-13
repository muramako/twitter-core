# 更新（存在しない `uid` の場合は新規登録）
`curl -X POST  -H 'Content-type: application/json' localhost:8983/solr/twitter/update?commit=true -d @update.json`

# 削除
`curl -X POST  -H 'Content-type: application/json' localhost:8983/solr/twitter/update?commit=true -d @delete.json`

# 検索
## ツイート検索
`curl -X GET 'localhost:8983/solr/twitter/select?indent=on&q=%E3%83%A1%E3%83%B3%E3%83%86&wt=json'`

## ユーザー検索
`curl -X GET 'localhost:8983/solr/twitter/select?fq=username:sample&indent=on&q=*:*&wt=json'`

