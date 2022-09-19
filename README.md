# README

This README would normally document whatever steps are necessary to get the
application up and running.

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

