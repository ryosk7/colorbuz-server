# README

## Setup
```
$ docker-compose build
$ docker-compose up
$ docker-compose run web rails db:create
$ docker-compose exec web rails db:migrate
# If your PC is Mac, you can use under command.
$ open http://localhost:8000
```

## For starter
```
$ docker-compose build
$ docker-compose up
$ docker-compose run web rails db:create
$ docker-compose exec web rails g scaffold posts
$ docker-compose exec web rails db:migrate
# If your PC is Mac, you can use under command.
$ open http://localhost:8000/posts
```

## DB操作
以下に統一すること
```
# 新規にtableを追加する時
$ docker-compose exec web rails g model Sample string:sample
$ docker-compose exec web rails db:migrate

# 既存のtableに変更を加える時
# 対象のtableのmigrationファイルに変更を加えて、
$ docker-compose exec web rails db:migrate:reset
```