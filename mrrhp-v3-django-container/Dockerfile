# 既存の mrrhp v3 を Docker で動かしてみるための Dockerfile.
# NOTE: 現在の v3 は python 3.6 で動いているが、

# 他の image はこちら https://hub.docker.com/_/python
FROM python:3.7-alpine

WORKDIR /app

RUN apk update && \
    pip install --upgrade pip setuptools && \
    pip install pipenv

# NOTE: このポートを解放する意図である、というドキュメントとして機能するコマンドです。
#       ポートを実際に解放するコマンドではありません。
EXPOSE 8000
