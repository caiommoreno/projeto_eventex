# Eventex

Sistema de eventos encomendado pela Morena.

## Como desenvolver?

1. Clone o repositório;
2. Crie um virtualenv com Python 3.8;
3. Ative seu virtualenv;
4. Instale as dependências;
5. Configure a instância com o .env;
6. Execute os testes.

```console
git clone git@github.com:caiommoreno/eventex.git wttd
cd wttd
python -m venv .wttd
source .wttd/bin/activate #Unix/MAC
source .wttd/bin/activate.bat #Windows
pip install -r requirements.txt
cp contrib/env-sampe .env
python manage.py test
```

## Como fazer o deploy?

1. Crie uma instância no Heroku;
2. Evie as configurações para o Heroku;
3. Defina uma secret-key segura para a instância;
4. Defina DEBUG=False;
5. Configure o serviço de e-mail;
6. Envie o código para o Heroku.

```console
heroku create minhainstancia
heroku config:push
heroku config:set SECRET_KEY='python contrib/secret_gen.py'
heroku config:set DEBUG=False
# configurar email
git push heroku master --force
```