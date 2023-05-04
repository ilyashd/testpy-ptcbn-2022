# Instalasi dan Konfigurasi

### Soal no 1

## Yang harus di install

```
$ pip install django
$ pip install djangorestframework
$ pip install djangorestframework-jwt
```

## Yang harus ditambah di settings.py

```
import datetime

INSTALLED_APPS = [
 'rest_framework',
    'rest_framework_jwt',
    'users',
]

REST_FRAMEWORK = {
    'DEFAULT_PERMISSION_CLASSES': (
        'rest_framework.permissions.IsAuthenticated',
    ),
    'DEFAULT_AUTHENTICATION_CLASSES': (
        'rest_framework_jwt.authentication.JSONWebTokenAuthentication',
    ),
}

JWT_AUTH = {
    'JWT_EXPIRATION_DELTA': datetime.timedelta(days=7),
    'JWT_AUTH_HEADER_PREFIX': 'Bearer',
}
```

### Soal no 2

## Yang harus ditambah di settings.py

```
REST_FRAMEWORK = {
    'DEFAULT_PERMISSION_CLASSES': (
        'rest_framework.authentication.TokenAuthentication',
        )
     }
     
```

### Soal no 3

## Yang harus di install

```
$ pip install django-filter
$ pip install psycopg2
```

## Yang harus ditambah di settings.py

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'mydatabase',
        'USER': 'mydatabaseuser',
        'PASSWORD': 'mypassword',
        'HOST': 'localhost',
        'PORT': '5432',
        #Sesuai konfigurasi perangkat masing2
    }
}
