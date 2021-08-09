# Content to make programming better and faster

- [Content to make programming better and faster](#content-to-make-programming-better-and-faster)
  - [Django](#django)
    - [Authentication](#authentication)
    - [User registration](#user-registration)
  - [General information](#general-information)
  - [GIT](#git)
  - [Python](#python)
  - [SQL](#sql)
  - [Web](#web)

## Django

### Authentication

```python
## Default Authentication

REST_FRAMEWORK = {
    'DEFAULT_PERMISSION_CLASSES': [
        'rest_framework.permissions.IsAuthenticated',
    ],
    'DEFAULT_AUTHENTICATION_CLASSES': [ # new
        'rest_framework.authentication.SessionAuthentication',
        'rest_framework.authentication.BasicAuthentication',
        'rest_framework.authentication.TokenAuthentication', # new
], }




pipenv install dj-rest-auth==1.1.0

# config/settings.py

INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    # 3rd-party apps
    'rest_framework',
    'rest_framework.authtoken', # new
    'dj_rest_auth', # new



#config/urls.py

urlpatterns += [

    path('api-auth/', include('rest_framework.urls')),
    path('api/v1/dj-rest-auth/', include('dj_rest_auth.urls')), # new
]
```

- We have a working log in endpoint at <http://127.0.0.1:8000/api/v1/dj-rest-auth/login/>.
- And a log out endpoint at <http://127.0.0.1:8000/api/v1/dj-rest-auth/logout/>.

- There are also endpoints for password reset, which is located at: \
<http://127.0.0.1:8000/api/v1/dj-rest-auth/password/reset>
- We have a working log in endpoint at <http://127.0.0.1:8000/api/v1/dj-rest-auth/login/>.-  
- And a log out endpoint at <http://127.0.0.1:8000/api/v1/dj-rest-auth/logout/>.-  
- There are also endpoints for password reset, which is located at: \
  <http://127.0.0.1:8000/api/v1/dj-rest-auth/password/reset>

### User registration

```python
pipenv install django-allauth

 config/settings.py
INSTALLED_APPS += [
    'django.contrib.sites', # new
    # 3rd-party apps
    'rest_framework.authtoken',
    'allauth', # new
    'allauth.account', # new
    'allauth.socialaccount', # new
    'dj_rest_auth.registration', # new
]

EMAIL_BACKEND = 'django.core.mail.backends.console.EmailBackend' # new
SITE_ID = 1 # new


urlpatterns += [
    path('api/v1/dj-rest-auth/registration/', include('dj_rest_auth.registration.urls')), # new
]
```

- There is now a user registration endpoint at \
  <http://127.0.0.1:8000/api/v1/dj-rest-auth/registration/>.


## General information

## GIT

## Python

## SQL

## Web

##
