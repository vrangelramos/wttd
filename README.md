# Eventex

Sistemas de Eventos encomendado pela Morena.

[![Build Status](https://travis-ci.org/vrangelramos/wttd.svg?branch=master)](https://travis-ci.org/vrangelramos/wttd)
[![Code Health](https://landscape.io/github/vrangelramos/wttd/master/landscape.svg?style=flat)](https://landscape.io/github/vrangelramos/wttd/master)

## Como desenvolver?

1. Clone o repositório.
2. Crie um virtualenv com Python 3.5
3. Ative o virtualenv.
4. Instale as dependências.
5. Configure a instância com o .env
6. Execute os testes.

```console
git clone git@github.com:victorramos/eventex.git wttd
cd wttd
python -m venv .wttd
.wttd/Sources/activate.bat
pip install -r requirements-dev.txt
cp contrib/env-example .env
python manage.py test
```

## Como fazer o deploy?

1. Crie uma instância no heroku
2. Envie as configurações para o heroku
3. Define uma SECRET_KEY segura para instância
4. Defina DEBUG=False
5. Configure o serviço de email
6. Envie o código para o heroku

```
heroku create minhainstancia
heroku config:push
heroku config:set SECRET_KEY='python contrib/sercret_gen.py'
heroku config:set DEBUG=False
# configuro o email
gir push heroku master --force
```