# laravel-project

## docker 初期設定
他のdocker-composeと連携する場合は下記を作成しておくこと
```
docker network create local-network
```

## laravelの.env作成
```
docker compose exec app cp .env.example .env
```

## composer install
```
docker compose exec app composer install
```

## (フロントもある場合) npm関連
```
docker compose exec app npm ci && npm build
```

## DB構築 

```
php artisan migrate --seed
```
