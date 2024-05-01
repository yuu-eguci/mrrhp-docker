mrrhp-docker
===

🐳 この Docker repository は、 mrrhp-apache を Docker 環境で動かすためにある!

## Branches

- v3: 開発終了
- v4: 稼働中

## Installation

```bash
# Clone mrrhp-docker and mrrhp-apache
git clone git@github.com:yuu-eguci/mrrhp-apache.git ./app/mrrhp-apache

# Create containers
docker compose up -d

# Django log を見る
docker compose logs -f --tail=10 django-service

# Enter in the container
docker compose exec django-service sh

# For mrrhp-apache v3
pip install -r ./requirements.txt

# For mrrhp-apache v4 (PIPENV_VENV_IN_PROJECT を設定しているので venv はプロジェクト内に作成される)
pipenv sync --dev
```
