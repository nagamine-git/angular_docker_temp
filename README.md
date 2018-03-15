## ビルド・アプリ構築まで
```bash
# git clone
git clone https://github.com/nagaminenot/angular_docker_temp
# build
docker-compose build
# ng new
docker-compose -f docker-compose.yml -f docker-compose.init.yml up
```

## 起動
```bash
# サービスの立ち上げ（http://localhost:4200 からアクセス可能）
docker-compose -f docker-compose.yml -f docker-compose.serv.yml up
```

## コンテナのbashへの入り方
```bash
docker exec -it vitacedocker_angular_1 bash
```

## テストの仕方
```bash
# コンテナのbashに入った状態で以下を実行し、http://localhost:9876 をChromeで表示し、ソース更新する
ng test --poll=2000
```