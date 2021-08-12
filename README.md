> Make Programming Better

- [1. General information](#1-general-information)
- [2. GIT](#2-git)
  - [2.1. Cheat sheet](#21-cheat-sheet)
    - [2.1.1. Local Changes](#211-local-changes)
    - [2.1.2. Branches](#212-branches)
    - [2.1.3. Commit History](#213-commit-history)
    - [2.1.4. Rebase](#214-rebase)
    - [2.1.5. Undo](#215-undo)
    - [2.1.6. Tags](#216-tags)
    - [2.1.7. Repository Setup](#217-repository-setup)
    - [2.1.8. Global Config](#218-global-config)
  - [2.2. RE-clone](#22-re-clone)
  - [2.3. Clean and reset](#23-clean-and-reset)
  - [2.4. Clean](#24-clean)
  - [2.5. Reset](#25-reset)
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
    - [3.2.2. 3.2.2 XLSX Generators](#322-322-xlsx-generators)
- [4. Django](#4-django)
  - [4.1. Authentication](#41-authentication)
  - [4.2. User registration](#42-user-registration)
- [5. SQL](#5-sql)
- [6. Web](#6-web)

# 1. General information

# 2. GIT

## 2.1. Cheat sheet

### 2.1.1. Local Changes

Display the status of modified files

`git status`
Add a file to staging as it looks right now

`git add [file_name]`
Add a folder to staging as it looks right now

`git add [folder_name]`
Commit staged files in a new commit

`git commit -m "descriptive_message"`
Add all files to staging and commit them at once

`git commit -am "descriptive_message"`
Unstage a file while retaining the changes

`git reset [file_name]`
Diff of what is changed but not staged

`git diff`
Diff of what has changed between staged changes and the last commit

`git diff --staged`

### 2.1.2. Branches

List all branches. The current one is marked with *

`git branch`
Create a new branch

`git branch [branch_name]`
Switch to a branch

`git checkout [branch_name]`
Create a new branch and switch to it

`git checkout -b [branch_name]`
Switch to the previously checked out branch

`git checkout -`
Rename a branch

`git checkout -m [new_branch]`
Delete a branch, locally

`git branch -d [branch_name]`
Merge another branch into the current one

`git merge [branch_name]`
Working with a Remote Repository
Fetch and merge all commits from the tracked remote branch

`git pull`
Fetch and merge all commits from a specific remote branch

`git pull [alias] [branch_name]`
Fetch recent changes from the tracked remote branch but don't merge them

`git fetch`
Push all local branch commits to the tracked remote branch

`git push`
Push all local branch commits to a specific remote branch

`git push [alias] [branch_name]`
Add a new remote repository with the given alias

git remote add [alias] [repo_url]
Display a list of remote repositories and their URLs

`git remote -v`

### 2.1.3. Commit History

Show all commits in the current branch’s history

`git log`
Show all commits in the current branch’s history by printing each commit on a single line

`git log --oneline`
Show number of commits per author on all branches, excluding merge commits.

`git shortlog -s -n --all --no-merges`
Show number of commits per author on a branch, excluding merge commits.

`git shortlog -s -n [branch_name] --no-merges`
Show number of commits per author on all branches, including merge commits.

`git shortlog -s -n --all`
Show number of commits per author on a branch, including merge commits.

`git shortlog -s -n [branch_name]`

### 2.1.4. Rebase

Reapply commits from the current branch on top of another base

`git rebase [branch_name]`
Abort a rebase

`git rebase –-abort`
Continue a rebase after resolving conflicts

`git rebase –-continue`

### 2.1.5. Undo

Revert the changes in a commit and record them in a new commit

`git revert [commit]`
Reset to a previous commit and preserve the changes made since [commit] as unstaged

`git reset [commit]`
Reset to a previous commit and discard the changes made since the [commit]

`git reset --hard [commit]`
Stash
Stash modified and staged changes

`git stash`
Stash modified and staged changes with a custom message

`git stash push -m "message"`
Stash a selected file by specifying a path

`git stash push src/custom.css`
List all stashed changesets

`git stash list`
Restore the most recently stashed changeset and delete it

`git stash pop`
Delete the most recently stashed changeset

`git stash drop`

### 2.1.6. Tags

Create a new tag

`git tag "tagname"`
List all tags

`git tag`
Delete a tag

`git tag -d "tagname"`

### 2.1.7. Repository Setup

Create an empty repository in the current folder

`git init`
Create an empty repository in a specific folder

`git init [folder_name]`
Clone a repository and add it to the current folder

`git clone [repo_url]`
Clone a repository to a specific folder

`git clone [repo_url] [folder_name]`

### 2.1.8. Global Config

Set the username

`git config --global user.name "user_name"`
Set the user email

`git config --global user.email "user_email"`
Set automatic command line coloring

`git config --global color.ui auto`

## 2.2. RE-clone

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

## 2.3. Clean and reset

```bash
git clean --force -d -x
git reset --hard
```

- ❌ Deletes local, non-pushed commits
- ✅ Reverts changes you made to tracked files
- ✅ Restores tracked files you deleted
- ✅ Deletes files/dirs listed in .gitignore (like build files)
- ✅ Deletes files/dirs that are not tracked and not in .gitignore

## 2.4. Clean

```bash
git clean --force -d -x
```

- ❌ Deletes local, non-pushed commits
- ❌ Reverts changes you made to tracked files
- ❌ Restores tracked files you deleted
- ✅ Deletes files/dirs listed in .gitignore (like build files)
- ✅ Deletes files/dirs that are not tracked and not in .gitignore

## 2.5. Reset

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

### 3.2.2. 3.2.2 XLSX Generators  

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
