Dev: Marco Sena
Creditos: :Professora  Letícia Lima 

# Preparando o ambiente no django
### 1-Criar o ambiente virtual Linux/Windows

Windows
python -m venv .venv source 


msena@DESKTOP-NU65P6S MINGW64 /d/Projetos/site_empresa (main)
```
$ python -m venv .venv
```


### Ativar ambiente

msena@DESKTOP-NU65P6S MINGW64 /d/Projetos/site_empresa (main)
```
$ source .venv/Scripts/activate
```

## Linux  

## Caso não tenha virtualenv. "pip install virtualenv"
```
virtualenv .venv
```

#### Ativar ambiente
```
source .venv/bin/activate # Ativar ambiente

```


msena@DESKTOP-NU65P6S MINGW64 /d/Projetos/site_empresa (main)
```
$ python -m venv .venv
```

### Dica: Será criado uma pasta .venv


#### Instalar os seguintes pacotes Iniciais:

msena@DESKTOP-NU65P6S MINGW64 /d/Projetos/site_empresa (main)
```
 pip install django
```

msena@DESKTOP-NU65P6S MINGW64 /d/Projetos/site_empresa (main)
```
pip install pillow # tratamento de imagem
```


### Para criar o arquivo requirements.txt
`
#### Cria o arquivo contendo todas as dependências do nosso projeto
```
pip freeze > requirements.txt

```

#### Para criar as dependências lendo o arquivo requirements.txt
#### pip install -r requirements.txt

### seria instalado as dependecias baseada nesse arquivo  

#### Criando o projeto chamado Core

“core” é nome do seu projeto e quando colocamos um “.” depois do nome do projeto significa que é para criar os arquivos na raiz da pasta. Assim não cria subpasta do projeto

```
django-admin startproject core .
```

#### Testar a aplicação

```
python manage.py runserver
```

Output
```
$ python manage.py runserver
Watching for file changes with StatReloader
Performing system checks...

System check identified no issues (0 silenced).

You have 18 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
Run 'python manage.py migrate' to apply them.
November 06, 2023 - 06:56:05
Django version 4.2.7, using settings 'core.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CTRL-BREAK.

[06/Nov/2023 06:56:39] "GET / HTTP/1.1" 200 10664
Not Found: /favicon.ico
[06/Nov/2023 06:56:39] "GET /favicon.ico HTTP/1.1" 404 2108
[06/Nov/2023 06:56:55] "GET / HTTP/1.1" 200 10664

```

Dica: Será dado uma alerta sobre as migrações, não se preocupe nesse momento.
Deve ser copiado o endereço http no browse, deve ser aberto uma pagina do djago se tudo deu certo.   

### Criando a 1ª Branch do projeto

```
git checkout -b parte01_config_static



msena@DESKTOP-NU65P6S MINGW64 /d/Projetos/site_empresa (main)
