## 初回設定
```bash
# git clone
git clone https://github.com/nagaminenot/vitace_docker
# logsディレクトリを用意する
mkdir logs
# buildする
docker-compose build
# npm installしたりする
docker-compose -f docker-compose.yml -f docker-compose.init.yml up
```

## 起動
```bash
# サービスの立ち上げ（http://localhost:4200 からアクセス可能）
docker-compose -f docker-compose.yml -f docker-compose.serv.yml up
```

## bashへの入り方
```bash
docker exec -it vitacedocker_angular_1 bash
```

## テストの仕方
```bash
# bashに入った状態で以下を叩き、http://localhost:9876 を叩いたり、ソースを変更したりする
ng test --poll=2000
```