# Content to make programming better and faster

- [Content to make programming better and faster](#content-to-make-programming-better-and-faster)
  - [Django](#django)
    - [Authentication](#authentication)
    - [User registration](#user-registration)
  - [General information](#general-information)
  - [GIT](#git)
    - [RE-clone](#re-clone)
    - [Clean and reset](#clean-and-reset)
    - [Clean](#clean)
    - [Reset](#reset)
  - [Python](#python)
    - [Data Types](#data-types)
      - [Text Type: `str`](#text-type-str)
      - [Numeric Types: `int`, `float`, `complex`](#numeric-types-int-float-complex)
      - [Sequence Types: `list`, `tuple`, `range`](#sequence-types-list-tuple-range)
        - [List](#list)
          - [Transform a nested list into a simple list](#transform-a-nested-list-into-a-simple-list)
  - [Mapping Type: `dict`](#mapping-type-dict)
  - [Set Types: `set`, `frozenset`](#set-types-set-frozenset)
  - [Boolean Type: `bool`](#boolean-type-bool)
  - [Binary Types: `bytes`, `bytearray`, `memoryview`](#binary-types-bytes-bytearray-memoryview)
  - [Text Type: `str`](#text-type-str-1)
  - [Numeric Types: `int`, `float`, `complex`](#numeric-types-int-float-complex-1)
  - [Sequence Types: `list`, `tuple`, `range`](#sequence-types-list-tuple-range-1)
    - [List](#list-1)
      - [Transform a nested list into a simple list](#transform-a-nested-list-into-a-simple-list-1)
  - [Mapping Type: `dict`](#mapping-type-dict-1)
  - [Set Types: `set`, `frozenset`](#set-types-set-frozenset-1)
  - [Boolean Type: `bool`](#boolean-type-bool-1)
  - [Binary Types: `bytes`, `bytearray`, `memoryview`](#binary-types-bytes-bytearray-memoryview-1)
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

### RE-clone

```bash
GIT=$(git rev-parse --show-toplevel)
cd $GIT/..
rm -rf $GIT
git clone ...
```

- ✅ Deletes local, non-pushed commits
- ✅ Reverts changes you made to tracked files
- ✅ Restores tracked files you deleted
- ✅ Deletes files/dirs listed in .gitignore (like build files)
- ✅ Deletes files/dirs that are not tracked and not in .gitignore
- 😀 You won't forget this approach
- 😔 Wastes bandwidth

### Clean and reset

```bash
git clean --force -d -x
git reset --hard
```

- ❌ Deletes local, non-pushed commits
- ✅ Reverts changes you made to tracked files
- ✅ Restores tracked files you deleted
- ✅ Deletes files/dirs listed in .gitignore (like build files)
- ✅ Deletes files/dirs that are not tracked and not in .gitignore

### Clean

```bash
git clean --force -d -x
```

- ❌ Deletes local, non-pushed commits
- ❌ Reverts changes you made to tracked files
- ❌ Restores tracked files you deleted
- ✅ Deletes files/dirs listed in .gitignore (like build files)
- ✅ Deletes files/dirs that are not tracked and not in .gitignore

### Reset

```bash
git reset --hard
```

- ❌ Deletes local, non-pushed commits
- ✅ Reverts changes you made to tracked files
- ✅ Restores tracked files you deleted
- ❌ Deletes files/dirs listed in .gitignore (like build files)
- ❌ Deletes files/dirs that are not tracked and not in .gitignore

## Python

### Data Types

#### Text Type: `str`

#### Numeric Types: `int`, `float`, `complex`

#### Sequence Types: `list`, `tuple`, `range`

##### List

###### Transform a nested list into a simple list

```python
from functools import reduce

nested_list = [[1], [2], [3, 5, 6], [4, 3, 12, 33]]

simple_list = reduce(lambda x,y: x+y, nested_list)
```

## Mapping Type: `dict`

## Set Types: `set`, `frozenset`

## Boolean Type: `bool`

## Binary Types: `bytes`, `bytearray`, `memoryview`

## Text Type: `str`

## Numeric Types: `int`, `float`, `complex`

## Sequence Types: `list`, `tuple`, `range`

### List

#### Transform a nested list into a simple list

```python
from functools import reduce

nested_list = [[1], [2], [3, 5, 6], [4, 3, 12, 33]]

simple_list = reduce(lambda x,y: x+y, nested_list)
```

## Mapping Type: `dict`

## Set Types: `set`, `frozenset`

## Boolean Type: `bool`

## Binary Types: `bytes`, `bytearray`, `memoryview`

## SQL

## Web

##
