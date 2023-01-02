mrrhp-docker
===

🐳 この Docker repository は、 mrrhp-apache を Docker 環境で動かすためにある!

```bash
# Clone mrrhp-apache
git clone git@github.com:yuu-eguci/mrrhp-apache.git ./app/mrrhp-apache

# Create containers
docker-compose up -d

# Enter in the container
docker-compose exec django-service sh

# For mrrhp-apache v3
pip install -r ./requirements.txt
```
