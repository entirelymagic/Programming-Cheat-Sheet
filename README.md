> Make Programming Better

- [1. General information](#1-general-information)
- [2. GIT](#2-git)
  - [2.1. RE-clone](#21-re-clone)
  - [2.2. Clean and reset](#22-clean-and-reset)
  - [2.3. Clean](#23-clean)
  - [2.4. Reset](#24-reset)
- [3. Python](#3-python)
  - [3.1. Data Types](#31-data-types)
    - [3.1.1. Text Type: `str`](#311-text-type-str)
    - [3.1.2. Numeric Types: `int`, `float`, `complex`](#312-numeric-types-int-float-complex)
    - [3.1.3. Sequence Types: `list`, `tuple`, `range`](#313-sequence-types-list-tuple-range)
      - [3.1.3.1. List](#3131-list)
        - [3.1.3.1.1. Transform a nested list into a simple list](#31311-transform-a-nested-list-into-a-simple-list)
    - [3.1.4. Mapping Type: `dict`](#314-mapping-type-dict)
    - [3.1.5. Set Types: `set`, `frozenset`](#315-set-types-set-frozenset)
    - [3.1.6. Boolean Type: `bool`](#316-boolean-type-bool)
    - [3.1.7. Binary Types: `bytes`, `bytearray`, `memoryview`](#317-binary-types-bytes-bytearray-memoryview)
  - [3.2. Generators](#32-generators)
    - [3.2.1. EAN generators](#321-ean-generators)
    - [3.2.2 XLSX Generators](#322-xlsx-generators)
- [4. Django](#4-django)
  - [4.1. Authentication](#41-authentication)
  - [4.2. User registration](#42-user-registration)
- [5. SQL](#5-sql)
- [6. Web](#6-web)

# 1. General information

# 2. GIT

## 2.1. RE-clone

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

## 2.2. Clean and reset

```bash
git clean --force -d -x
git reset --hard
```

- ❌ Deletes local, non-pushed commits
- ✅ Reverts changes you made to tracked files
- ✅ Restores tracked files you deleted
- ✅ Deletes files/dirs listed in .gitignore (like build files)
- ✅ Deletes files/dirs that are not tracked and not in .gitignore

## 2.3. Clean

```bash
git clean --force -d -x
```

- ❌ Deletes local, non-pushed commits
- ❌ Reverts changes you made to tracked files
- ❌ Restores tracked files you deleted
- ✅ Deletes files/dirs listed in .gitignore (like build files)
- ✅ Deletes files/dirs that are not tracked and not in .gitignore

## 2.4. Reset

```bash
git reset --hard
```

- ❌ Deletes local, non-pushed commits
- ✅ Reverts changes you made to tracked files
- ✅ Restores tracked files you deleted
- ❌ Deletes files/dirs listed in .gitignore (like build files)
- ❌ Deletes files/dirs that are not tracked and not in .gitignore

# 3. Python

## 3.1. Data Types

### 3.1.1. Text Type: `str`

### 3.1.2. Numeric Types: `int`, `float`, `complex`

### 3.1.3. Sequence Types: `list`, `tuple`, `range`

#### 3.1.3.1. List

##### 3.1.3.1.1. Transform a nested list into a simple list

```python
from functools import reduce

nested_list = [[1], [2], [3, 5, 6], [4, 3, 12, 33]]

simple_list = reduce(lambda x,y: x+y, nested_list)
```

### 3.1.4. Mapping Type: `dict`

### 3.1.5. Set Types: `set`, `frozenset`

### 3.1.6. Boolean Type: `bool`

### 3.1.7. Binary Types: `bytes`, `bytearray`, `memoryview`

## 3.2. Generators

### 3.2.1. EAN generators

Generate EAN 13 barcodes for products.

Formula used (5940000 + random_number + last digit validator)

EAN country codes : <https://wholesgame.com/trade-info/ean-barcodes-country/>

- Romania country code: 594
Barcode number generation using faker:
- <https://faker.readthedocs.io/en/master/providers/faker.providers.barcode.html>
Barcode Image generation:
- <https://python-barcode.readthedocs.io/en/stable/>
- `python-barcode==0.13.1`

### 3.2.2 XLSX Generators  

- **XlsxWriter**8:  Only for generating NEW files.

  `pip install XlsxWriter`

  <https://xlsxwriter.readthedocs.io/index.html>

# 4. Django

## 4.1. Authentication

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

## 4.2. User registration

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

- There is now a user registration endpoint at  F
  <http://127.0.0.1:8000/api/v1/dj-rest-auth/registration/>.

# 5. SQL

# 6. Web
