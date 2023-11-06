Dev: Marco Sena
Creditos: :Professora  Letícia Lima 

# Arquivos static

#### Vamos salvar o nosso estado atual e atualizar o repositorio (caso ainda não tenha feito) 

```
$ git add ..

$ git commit -m "Preparando o ambiente virtual" # Fazendo o cmommit local

$ git push                                      # Atualizando o repostitorio

```

#### Criar uma nova branch  
```
$ git checkout -b p01_config_static
```

## ALTERAR o arqivo core/setting.py
import os

### base_dir config

BASE_DIR = os.path.dirname(os.path.dirname(os.path.abspath(__file__)))
TEMPLATE_DIR = os.path.join(BASE_DIR,'templates')
STATIC_DIR=os.path.join(BASE_DIR,'static')

### Database
```
# Banco de Dados.
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': os.path.join(BASE_DIR, os.getenv('NAME_DB')),
        #'USER':os.getenv('USER_DB')
        #'PASSWORD': os.getenv('PASSWORD_DB')
        #'HOST':os.getenv('HOST_DB')
        #'PORT':os.getenv('PORT_DB')
    }
}
```


```
STATIC_ROOT = os.path.join(BASE_DIR,'static')
STATIC_URL = '/static/'
```


```
# STATICFILES_DIRS = [ # talvez em Produção podesse usar assim.
#    BASE_DIR / 'static',
# ]

MEDIA_ROOT=os.path.join(BASE_DIR,'media')
MEDIA_URL = '/media/'
```

### Internationalization
### Se quiser deixar em PT BR
```
LANGUAGE_CODE = 'pt-br'
TIME_ZONE = 'America/Sao_Paulo'
USE_I18N = True
USE_L10N = True
USE_TZ = True
```

####  Em um ambiente de produção, 
É comum usar um serviço de CDN para fornecer
arquivos estáticos em vez de servir diretamente do servidor Django, nesse caso, pode
ser necessário configurar o STATICFILES_DIRS para incluir outros diretórios onde os
arquivos estáticos estão localizados.

#### core/urls.py

```
from django.contrib import admin
from django.conf import settings
from django.conf.urls.static import static
from django.urls import path
urlpatterns = [
path('admin/', admin.site.urls),
]
urlpatterns += static(settings.STATIC_URL, document_root=settings.STATIC_ROOT)
urlpatterns += static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)

```

#### Atualizando o repositório remoto
```
git add .
```

```

git commit -m "configurando os arquivos statics"
```
```

git push origin p01_config_static 
```

#### Fazendo o merge (atualizando o main)
#### 1-Muda para branch principal

```
$ git checkout main
```

#### 2-Faz o merge

```
msena@DESKTOP-NU65P6S MINGW64 /d/Projetos/site_empresa (main)

$ git merge p01_config_static
```

OUTPUT
```
Updating a60bfa7..3ae18ac
Fast-forward
 core/settings.py                         | 37 ++++++++----
 core/urls.py                             |  5 ++
 docs/1-Ambiente_virtual_Linux_windows.md | 11 +---
 docs/2-Arquivos STATIC.md                | 98 ++++++++++++++++++++++++++++++++
 4 files changed, 131 insertions(+), 20 deletions(-)
 create mode 100644 docs/2-Arquivos STATIC.md
(.venv) 
```

#### 3-Verificamos onde estamos

```
msena@DESKTOP-NU65P6S MINGW64 /d/Projetos/site_empresa (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
(.venv)
```

#### 4-Enviando para o repositório remoto
```
msena@DESKTOP-NU65P6S MINGW64 /d/Projetos/site_empresa (main)
$ git push
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/MarcoSena2210/site_empresa.git
   a60bfa7..3ae18ac  main -> main
(.venv)
```

*** A professora faz as alterações depois cria a branch,
