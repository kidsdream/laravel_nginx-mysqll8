# Name
laravel_nginx-mysql8

# Note
docker/nginx/default.confのコメントに
プロジェクト名を記入する。

docker-compose.ymlのenvironmentに
初期生成時のDBやユーザ情報を入力すると作成できる。

`docker-compose exec php bash`コマンドでPHP環境に入る。
/var/www/html配下にて、`composer create-project "laravel/laravel=6.0.*" --prefer-dist {プロジェクト名}`コマンド
これでLaravel環境ができる。
※この時点でLravelトップページが表示できるはず。

## DB接続手順
```
DB_CONNECTION=mysql
DB_HOST=db
DB_PORT=3306
DB_DATABASE=laravel_db
DB_USERNAME=laraveluser
DB_PASSWORD=laravel_pass
```
