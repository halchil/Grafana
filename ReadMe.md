# はじめに
はじめに


# 事前準備

## ネットワーク作成

```
[実行コマンド]
docker network create --subnet=172.10.10.0/24 --gateway=172.10.10.1 ecosystem
```

## volume 作成
```
[実行コマンド]
docker volume create grafana-data
```

## hostsファイル登録

`val-ecosystem.com`


# デプロイ

```
docker compose -f grafana-deploy.yaml up -d
docker compose -f nginx-deploy.yaml up -d
```

# 確認

IPアドレス