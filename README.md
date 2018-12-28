# NginxでBASIC認証なリバースプロキシを作るためのdocker-compose.ymlなど

## 使い方

### 設定

    cp dotenv-example .env
    vim .env

    docker run --rm nginx:latest echo "ユーザー名:$(openssl passwd -apr1 パスワード)" >> htpasswd

### 起動

    docker-compose up -d

### 停止

    docker-compose down

### ログ確認

    docker-compose logs -ft
