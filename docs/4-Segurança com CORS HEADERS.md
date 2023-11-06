
[Github](https://github.com/MarcoSena2210/web_empresa)

#### Créditos: Professora Letícia Lima (Udemy)



#### Atualizar o requireiment.txt
#### Como incluimos uma nova biblioteca precisamos atualizar o arquivo reuiriments.txt
```
pip freeze > requirements.txt
``` 

#### Criar uma nova branch  
```
$ git checkout -b p02_15.04_config_variaveis_ambiente
```


msena@DESKTOP-NU65P6S MINGW64 /d/Projetos/site_empresa (p02_15.04_config_variaveis_ambiente) 
```
$ git add .
```

msena@DESKTOP-NU65P6S MINGW64 /d/Projetos/site_empresa (p02_15.04_config_variaveis_ambiente) 

#### Salvando localmente
```
$ git commit -m "Configurando o arquivo de variaveis .env no settings.py"
```

#### OUTPUT 
```

[p02_15.04_config_variaveis_ambiente 3bc8c46] Configurando o arquivo de variaveis .env no settings.py
 615 files changed, 4918 insertions(+), 896 deletions(-)
 create mode 100644 .venv/Lib/site-packages/dotenv/__init__.py
 create mode 100644 .venv/Lib/site-packages/dotenv/__main__.py
 create mode 100644 .venv/Lib/site-packages/dotenv/__pycache__/__init__.cpython-312.pyc      
 create mode 100644 .venv/Lib/site-packages/dotenv/__pycache__/__main__.cpython-312.pyc      
 create mode 100644 .venv/Lib/site-packages/dotenv/__pycache__/cli.cpython-312.pyc
 create mode 100644 .venv/Lib/site-packages/dotenv/__pycache__/ipython.cpython-312.pyc       
 create mode 100644 .venv/Lib/site-packages/dotenv/__pycache__/main.cpython-312.pyc
 create mode 100644 .venv/Lib/site-packages/dotenv/__pycache__/parser.cpython-312.pyc        
 create mode 100644 .venv/Lib/site-packages/dotenv/__pycache__/variables.cpython-312.pyc     
 create mode 100644 .venv/Lib/site-packages/dotenv/__pycache__/version.cpython-312.pyc       
 create mode 100644 .venv/Lib/site-packages/dotenv/cli.py
 create mode 100644 .venv/Lib/site-packages/dotenv/ipython.py
 create mode 100644 .venv/Lib/site-packages/dotenv/main.py
 create mode 100644 .venv/Lib/site-packages/dotenv/parser.py
 create mode 100644 .venv/Lib/site-packages/dotenv/py.typed
 create mode 100644 .venv/Lib/site-packages/dotenv/variables.py
 create mode 100644 .venv/Lib/site-packages/dotenv/version.py
 rename .venv/Lib/site-packages/{pip-23.2.1.dist-info => pip-23.3.1.dist-info}/AUTHORS.txt (98%)
 rename .venv/Lib/site-packages/{pip-23.2.1.dist-info => pip-23.3.1.dist-info}/INSTALLER (100%)
 rename .venv/Lib/site-packages/{pip-23.2.1.dist-info => pip-23.3.1.dist-info}/LICENSE.txt (100%)
 rename .venv/Lib/site-packages/{pip-23.2.1.dist-info => pip-23.3.1.dist-info}/METADATA (81%) rename .venv/Lib/site-packages/{pip-23.2.1.dist-info => pip-23.3.1.dist-info}/RECORD (89%)  
 rename .venv/Lib/site-packages/{pip-23.2.1.dist-info => pip-23.3.1.dist-info}/REQUESTED (100%)
 rename .venv/Lib/site-packages/{pip-23.2.1.dist-info => pip-23.3.1.dist-info}/WHEEL (65%)   
 rename .venv/Lib/site-packages/{pip-23.2.1.dist-info => pip-23.3.1.dist-info}/entry_points.txt (100%)
 rename .venv/Lib/site-packages/{pip-23.2.1.dist-info => pip-23.3.1.dist-info}/top_level.txt 
(100%)
 delete mode 100644 .venv/Lib/site-packages/pip/_internal/utils/__pycache__/inject_securetransport.cpython-312.pyc
 delete mode 100644 .venv/Lib/site-packages/pip/_internal/utils/inject_securetransport.py    
 delete mode 100644 .venv/Lib/site-packages/pip/_vendor/cachecontrol/__pycache__/compat.cpython-312.pyc
 delete mode 100644 .venv/Lib/site-packages/pip/_vendor/cachecontrol/compat.py
 create mode 100644 .venv/Lib/site-packages/pip/_vendor/truststore/__init__.py
 create mode 100644 .venv/Lib/site-packages/pip/_vendor/truststore/__pycache__/__init__.cpython-312.pyc
 create mode 100644 .venv/Lib/site-packages/pip/_vendor/truststore/__pycache__/_api.cpython-312.pyc
 create mode 100644 .venv/Lib/site-packages/pip/_vendor/truststore/__pycache__/_macos.cpython-312.pyc
 create mode 100644 .venv/Lib/site-packages/pip/_vendor/truststore/__pycache__/_openssl.cpython-312.pyc
 create mode 100644 .venv/Lib/site-packages/pip/_vendor/truststore/__pycache__/_ssl_constants.cpython-312.pyc
 create mode 100644 .venv/Lib/site-packages/pip/_vendor/truststore/__pycache__/_windows.cpython-312.pyc
 create mode 100644 .venv/Lib/site-packages/pip/_vendor/truststore/_api.py
 create mode 100644 .venv/Lib/site-packages/pip/_vendor/truststore/_macos.py
 create mode 100644 .venv/Lib/site-packages/pip/_vendor/truststore/_openssl.py
 create mode 100644 .venv/Lib/site-packages/pip/_vendor/truststore/_ssl_constants.py
 create mode 100644 .venv/Lib/site-packages/pip/_vendor/truststore/_windows.py
 create mode 100644 .venv/Lib/site-packages/python_dotenv-1.0.0.dist-info/INSTALLER
 create mode 100644 .venv/Lib/site-packages/python_dotenv-1.0.0.dist-info/LICENSE
 create mode 100644 .venv/Lib/site-packages/python_dotenv-1.0.0.dist-info/METADATA
 create mode 100644 .venv/Lib/site-packages/python_dotenv-1.0.0.dist-info/RECORD
 create mode 100644 .venv/Lib/site-packages/python_dotenv-1.0.0.dist-info/REQUESTED
 create mode 100644 .venv/Lib/site-packages/python_dotenv-1.0.0.dist-info/WHEEL
 create mode 100644 .venv/Lib/site-packages/python_dotenv-1.0.0.dist-info/entry_points.txt   
 create mode 100644 .venv/Lib/site-packages/python_dotenv-1.0.0.dist-info/top_level.txt      
 create mode 100644 .venv/Scripts/dotenv.exe
 create mode 100644 core/.env
 create mode 100644 core/_env
 create mode 100644 "docs/3-Vari\303\241veis de ambiente usando python-dotenv.md"
 create mode 100644 docs/Biblioteca_OS.png
```

#### Enviando para repositório remoto
(.venv)
msena@DESKTOP-NU65P6S MINGW64 /d/Projetos/site_empresa (p02_15.04_config_variaveis_ambiente) 
```
$ git push origin p02_15.04_config_variaveis_ambiente
```

#### OUTPUT
```
Enumerating objects: 890, done.
Counting objects: 100% (890/890), done.
Delta compression using up to 4 threads
Compressing objects: 100% (729/729), done.
Writing objects: 100% (735/735), 3.03 MiB | 1.67 MiB/s, done.
Total 735 (delta 139), reused 2 (delta 0), pack-reused 0     
remote: Resolving deltas: 100% (139/139), completed with 107 local objects.
remote: 
remote: Create a pull request for 'p02_15.04_config_variaveis_ambiente' on GitHub by visiting:
remote:      https://github.com/MarcoSena2210/site_empresa/pull/new/p02_15.04_config_variaveis_ambiente
remote: 
To https://github.com/MarcoSena2210/site_empresa.git
 * [new branch]      p02_15.04_config_variaveis_ambiente -> p02_15.04_config_variaveis_ambiente

(.venv) 
msena@DESKTOP-NU65P6S MINGW64 /d/Projetos/site_empresa (p02_15.04_config_variaveis_ambiente) 
$
```

#### Fazendo o merge (atualizando o main)
#### 1-Muda para branch principal

```
$ git checkout main
```

#### 2-Faz o merge

```
msena@DESKTOP-NU65P6S MINGW64 /d/Projetos/site_empresa (main)

$ git merge p02_15.04_config_variaveis_ambiente
```

#### 4-Enviando para o repositório remoto
```
msena@DESKTOP-NU65P6S MINGW64 /d/Projetos/site_empresa (main)
$ git push
```

### Para configurar os Cors Headers precisamos instalar uma biblioteca.

<https://pypi.org/project/django-cors-headers/>

O CORS (Cross-Origin Resource Sharing) é um mecanismo de segurança do navegador que impede que um
site acesse recursos em outro site por padrão. Isso é feito para proteger os usuários de possíveis
vulnerabilidades de segurança.

No entanto, às vezes é necessário permitir que um site acesse recursos em outro site. É aí que o CORS
Headers entra em jogo. O CORS Headers é uma biblioteca do Django que permite que você configure seu
servidor para permitir que um site acesse seus recursos.

Ao instalar o CORS Headers, você pode adicionar uma configuração simples no seu arquivo de configuração
(settings.py) para permitir que um site específico acesse seus recursos. Por exemplo, se você tiver um site
hospedado em "<http://meusite.com>" e quiser permitir que ele acesse seus recursos, você pode adicionar o
seguinte ao seu settings.py:


#### Instalar a Biblioteca na nossa aplicação
```
pip install django-cors-headers
```

#### Atualizar o arquivo requiments.txt
````
pip freeze > requirements.txt
```` 

#### importar a nossa biblioteca,no settings.py
```
from corsheaders.defaults import default_headers
```

## Adicionar no settings.py
```
INSTALLED_APPS = [
    ...,
    "corsheaders",
    ...,
]`

```
#### MIDDLEWARE

```
MIDDLEWARE = [
    ...,
    "corsheaders.middleware.CorsMiddleware",
    "django.middleware.common.CommonMiddleware",
    ...,
]

#### ALLOWED_HOSTS
```
ALLOWED_HOSTS = [
    'localhost',
    '127.0.0.1',
]



CORS_ALLOW_HEADERS = list(default_headers) + [
'X-Register',
]

# CORS Config

CORS_ORIGIN_ALLOW_ALL = True

# CORS_ORIGIN_ALLOW_ALL como True, o que permite que qualquer site acesse seus recursos

# Defina como False e adicione o site no CORS_ORIGIN_WHITELIST onde somente o site da lista acesse os seus recursos

CORS_ALLOW_CREDENTIALS = False
CORS_ORIGIN_WHITELIST = ['http://meusite.com',] # Lista.

#### Cookies
SSL and Cookies Vamos deixar configurado tambem. No final do video vamos fazer deploy.

doc: <https://docs.djangoproject.com/en/4.1/ref/settings/>
CORS HEADERS 2

if not DEBUG:
    SECURE_SSL_REDIRECT = True
    ADMINS = [(os.getenv('SUPER_USER'), os.getenv('EMAIL'))]
    SESSION_COOKIE_SECURE = True
    CSRF_COOKIE_SECURE = True

##### if not DEBUG: verifica

Se a aplicação está sendo executada em modo de depuração ( DEBUG=True ). Se DEBUG for
False , isso significa que a aplicação está sendo executada em um ambiente de produção, portanto, as
configurações de segurança devem ser aplicadas.

##### SECURE_SSL_REDIRECT

Direciona todas as solicitações HTTP para HTTPS.

##### ADMINS

É uma lista de tuplas que contêm informações sobre os administradores do site.
Se ocorrer um erro no site, um email será enviado para os endereços listados em ADMINS .

##### SESSION_COOKIE_SECURE

Garante que os cookies de sessão sejam definidos apenas em conexões HTTPS

##### CSRF_COOKIE_SECURE
```
    Garante que os cookies CSRF sejam definidos apenas em conexões HTTPS.
    Essas configurações ajudam a proteger a aplicação contra ataques de interceptação e garantem que as
    informações confidenciais do usuário sejam mantidas seguras.

Com essas configurações, você permitirá que o site "<http://meusite.com>" acesse seus recursos. É
importante lembrar que, para que isso funcione, o site que está acessando seus recursos também deve ter a
configuração CORS corre
```


### Criando a 3ª Branch do projeto
#### Criar uma nova branch  

```
$ git checkout -b p03_16.05_config_CORS
```
```
$ git add .
```

msena@DESKTOP-NU65P6S MINGW64 /d/Projetos/site_empresa (p03_16.05_config_CORS) 

#### Salvando localmente
```
 git commit -m "Configurando a segurança usando CORS, configurando no settings.py"

 git push origin p03_16.05_config_CORS
```


#### Fazendo o merge (atualizando o main)
#### 1-Muda para branch principal

```
git checkout main 
```

#### 2-Faz o merge

```
msena@DESKTOP-NU65P6S MINGW64 /d/Projetos/site_empresa (main)

$ git merge p02_15.04_config_variaveis_ambiente
```

#### 4-Enviando para o repositório remoto
```
msena@DESKTOP-NU65P6S MINGW64 /d/Projetos/site_empresa (main)
$ git push
```

