# README

This README would normally document whatever steps are necessary to get the
application up and running.

# 0. バージョン
- ruby -> 3.1.2
- rails -> 7.0.3.1

# 1. 環境構築
### 1-1. Gitリポジトリをクローン
git clone https://github.com/carbohydratepro/test_generator.git

cd test_generator

### 1-2. dockerイメージをbuild
docker-compose build

### 1-3. Dockerを起動
docker-compose up -d

### 1-4. コマンドを実行
docker-compose run web rake db:create

docker-compose run web bundle install

docker-compose run web bundle exec rake app:update:bin

### 1-5. localhost:3000にアクセス
Railsの画面が表示されていれば成功

# 2. 動作確認
### 2-1. サンプルを生成
docker-compose run web bin/rails g scaffold User name:string

docker-compose run web bin/rake db:migrate

### 2-2. localhost:3000/usersにアクセス
ユーザー名の登録・一覧表示・編集・削除ができることを確認



