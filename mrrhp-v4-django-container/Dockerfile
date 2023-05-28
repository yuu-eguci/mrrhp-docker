# 他の image はこちら https://hub.docker.com/_/python
FROM python:3.11-alpine

WORKDIR /app

RUN apk update && \
    # For mysqlclient.
    apk add --no-cache mariadb-dev gcc libc-dev mysql-client && \
    pip install --upgrade pip setuptools && \
    pip install pipenv

# 1. 依存パッケージを取得する。
# 2. DBのmigrationを実行する。
# 3. DBに初期データを入れる。
# 4. 取得できた後にサーバーを起動する。
CMD ["sh", "-c", "pipenv sync --dev; pipenv run python manage.py migrate; pipenv run server;"]

# NOTE: このポートを解放する意図である、というドキュメントとして機能するコマンドです。
#       ポートを実際に解放するコマンドではありません。
EXPOSE 8000
