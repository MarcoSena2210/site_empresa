# Usando Requestlog

#### Autor: Marco Sena :computer:
[Github](https://github.com/MarcoSena2210/web_empresa)
#### Créditos: Professora Letícia Lima (Udemy)

#### Django-requestlogs
O pacote django-requestlogs permite a gravação de logs de requisições HTTP em um
banco de dados. Isso pode ser útil para análise de desempenho e solução de
problemas. O pacote também fornece uma interface web para visualização dos logs.

Precisamos Instalar essa biblioteca.
Documentação: <https://pypi.org/project/django-requestlogs/>



#### Instalar a biblioteca Django-requestlogs
```
pip install django-requestlogs
```

#### Recriar o requiriments(Atualizar)
```
pip freeze > requirements.txt
```

#### Adicionar no core/settings.py

##### RMIDDLEWARE
```
MIDDLEWARE = [
    'requestlogs.middleware.RequestLogsMiddleware',
]
```

##### REST_FRAMEWORK
```
REST_FRAMEWORK={
    'EXCEPTION_HANDLER': 'requestlogs.views.exception_handler',
}
```

Documentação: <<https://docs.djangoproject.com/en/4.1/topics/logging/#topic-loggingparts-loggers>>

#### Logs
```
LOGGING = {
    'version': 1,
    'disable_existing_loggers': False,
    'handlers': {
        'requestlogs_to_file': {
            'level': 'INFO',
            'class': 'logging.FileHandler',
            'filename': 'info.log',
        },
    },
    'loggers': {
        'requestlogs': {
            'handlers': ['requestlogs_to_file'],
            'level': 'INFO',
            'propagate': False,
        },
    },
}
```

```
REQUESTLOGS = {
    'SECRETS': ['password', 'token'],
    'METHODS': ('PUT', 'PATCH', 'POST', 'DELETE'),
}

```

#### LOGS 2
No primeiro bloco de código, LOGGING , estão sendo definidos os parâmetros do logger
de informações para as requisições, que será gravado em um arquivo chamado
info.log .

No segundo bloco, REQUESTLOGS , estão sendo definidas as opções de gravação de logs
para as requisições, como as informações que devem ser ocultadas e quais
métodos HTTP devem ser registrados. exemplo senhas, token de cliente/sistema.
Quando precisamos gerar log em alguma rota, script qualquer função em expecifico
podemos chamar essa biblioteca logger e receber as informações no arquivo de .log
que configuramos.

Por exemplo. Na view podemos fazer um tratamento assim, cria uma Exception para
tratar os erros e enviar para nosso arquivo de log.

```
import logging
error_logger = logging.getLogger()
```

def sendmail(data):
...
..

try:
data = response.data
sendmail(data)
except Exception as e:
error_logger.error(str(e) + "|" + str(data))
...

Outro detalhe, em produção o arquivo info.log quando voce criar ele no linux
precisa ter permissões.
```
sudo chmod -R 777 path/info.log
```



### Criando a 4ª Branch do projeto
#### Criar uma nova branch  

```
  git checkout -b p04_17.06_config_requestLOG
```
```
  git add .
```

msena@DESKTOP-NU65P6S MINGW64 /d/Projetos/site_empresa (p04_17.06_config_requestLOG) 

#### Salvando localmente
```
 git commit -m "Configurando o log segurança usando requestlog, configurando no settings.py"

 git push origin p04_17.06_config_requestLOG
```


#### Fazendo o merge (atualizando o main)
#### 1-Muda para branch principal

```
git checkout main 
```

#### 2-Faz o merge

```
msena@DESKTOP-NU65P6S MINGW64 /d/Projetos/site_empresa (main)

$ git merge p04_17.06_config_requestLOG
```

#### 4-Enviando para o repositório remoto
```
msena@DESKTOP-NU65P6S MINGW64 /d/Projetos/site_empresa (main)
$ git push
```

