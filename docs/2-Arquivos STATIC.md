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
``````
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

**core/urls.py**
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
### Atualizando
```
git add .

git commit -m "configurando os arquivos statics"

git push origin p01_config_static 
```