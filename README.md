# laravelとdocker、scssの環境構築テンプレート

## 環境構築
- Dockerビルド
  1. git clone git@github.com:taku0127/laravel-temp.git
  2. docker-compose up -d --build
  ※MySQLは、OSによって起動しない場合があるのでそれぞれのPCに合わせて docker-compose.yml ファイルを編集してください。
- Laravel環境構築
  1. docker-compose exec php bash
  2. composer install
  3. .env.exampleファイルから.envをコピーし、環境変数を設定
  4. php artisan key:generate
  5. chmod -R 777 ./*
  6. php artisan migrate
  7. php artisan db:seed
- sassの仕様
  1. cd src/ (srcディレクトリに入る)
  2. npm install
  3. npm run watch
  4. src/resources/scss/配下で編集
 
## 使用技術(実行環境)
- Laravel 8.83
- PHP 7.4
- MySQL 8.0

## URL
- 開発環境：http://localhost/
- 開発環境(phpmyadmin)：http://localhost:8080/
