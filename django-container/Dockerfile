# 他の image はこちら https://hub.docker.com/_/python
FROM python:3.10-alpine

WORKDIR /app

# For using argon2, https://ja.stackoverflow.com/questions/42881/docker-pythonalpine%E3%81%A7cffi%E3%81%AE%E3%82%B3%E3%83%B3%E3%83%91%E3%82%A4%E3%83%AB%E3%81%AB%E5%A4%B1%E6%95%97%E3%81%99%E3%82%8B
RUN apk update && \
    apk add build-base libffi-dev && \
    # For mysqlclient.
    apk add --no-cache mariadb-dev gcc libc-dev mysql-client && \
    pip install --upgrade pip && \
    pip install pipenv

# NOTE: このポートを解放する意図である、というドキュメントとして機能するコマンドです。
#       ポートを実際に解放するコマンドではありません。
EXPOSE 8000
