> Make Programming Better

- [1. General information](#1-general-information)
- [2. GIT](#2-git)
  - [2.1. Cheat sheet](#21-cheat-sheet)
    - [2.1.1. Local Changes](#211-local-changes)
      - [2.1.1.1. Display the status of modified files](#2111-display-the-status-of-modified-files)
      - [2.1.1.2. Add a file to staging as it looks right now](#2112-add-a-file-to-staging-as-it-looks-right-now)
      - [2.1.1.3. Add a folder to staging as it looks right now](#2113-add-a-folder-to-staging-as-it-looks-right-now)
      - [2.1.1.4. Commit staged files in a new commit](#2114-commit-staged-files-in-a-new-commit)
      - [2.1.1.5. Add all files to staging and commit them at once](#2115-add-all-files-to-staging-and-commit-them-at-once)
      - [2.1.1.6. Unstage a file while retaining the changes](#2116-unstage-a-file-while-retaining-the-changes)
      - [2.1.1.7. Diff of what is changed but not staged](#2117-diff-of-what-is-changed-but-not-staged)
      - [2.1.1.8. Diff of what has changed between staged changes and the last commit](#2118-diff-of-what-has-changed-between-staged-changes-and-the-last-commit)
    - [2.1.2. Branches](#212-branches)
      - [2.1.2.1. List all branches. The current one is marked with *](#2121-list-all-branches-the-current-one-is-marked-with-)
      - [2.1.2.2. Create a new branch](#2122-create-a-new-branch)
      - [2.1.2.3. Switch to a branch](#2123-switch-to-a-branch)
      - [2.1.2.4. Create a new branch and switch to it](#2124-create-a-new-branch-and-switch-to-it)
      - [2.1.2.5. Switch to the previously checked out branch](#2125-switch-to-the-previously-checked-out-branch)
      - [2.1.2.6. Rename a branch](#2126-rename-a-branch)
      - [2.1.2.7. Delete a branch, locally](#2127-delete-a-branch-locally)
      - [2.1.2.8. Merge another branch into the current one](#2128-merge-another-branch-into-the-current-one)
    - [2.1.3. Working with a Remote Repository](#213-working-with-a-remote-repository)
      - [2.1.3.1. Fetch and merge all commits from the tracked remote branch](#2131-fetch-and-merge-all-commits-from-the-tracked-remote-branch)
      - [2.1.3.2. Fetch and merge all commits from a specific remote branch](#2132-fetch-and-merge-all-commits-from-a-specific-remote-branch)
      - [2.1.3.3. Fetch recent changes from the tracked remote branch but don't merge them](#2133-fetch-recent-changes-from-the-tracked-remote-branch-but-dont-merge-them)
      - [2.1.3.4. Push all local branch commits to the tracked remote branch](#2134-push-all-local-branch-commits-to-the-tracked-remote-branch)
      - [2.1.3.5. Push all local branch commits to a specific remote branch](#2135-push-all-local-branch-commits-to-a-specific-remote-branch)
      - [2.1.3.6. Add a new remote repository with the given alias](#2136-add-a-new-remote-repository-with-the-given-alias)
      - [2.1.3.7. Display a list of remote repositories and their URLs](#2137-display-a-list-of-remote-repositories-and-their-urls)
    - [2.1.4. Commit History](#214-commit-history)
      - [2.1.4.1. Show all commits in the current branch’s history](#2141-show-all-commits-in-the-current-branchs-history)
      - [2.1.4.2. Show all commits in the current branch’s history by printing each commit on a single line](#2142-show-all-commits-in-the-current-branchs-history-by-printing-each-commit-on-a-single-line)
      - [2.1.4.3. Show number of commits per author on all branches, excluding merge commits](#2143-show-number-of-commits-per-author-on-all-branches-excluding-merge-commits)
      - [2.1.4.4. Show number of commits per author on a branch, excluding merge commits](#2144-show-number-of-commits-per-author-on-a-branch-excluding-merge-commits)
      - [2.1.4.5. Show number of commits per author on all branches, including merge commits](#2145-show-number-of-commits-per-author-on-all-branches-including-merge-commits)
      - [2.1.4.6. Show number of commits per author on a branch, including merge commits](#2146-show-number-of-commits-per-author-on-a-branch-including-merge-commits)
    - [2.1.5. Rebase](#215-rebase)
      - [2.1.5.1. Reapply commits from the current branch on top of another base](#2151-reapply-commits-from-the-current-branch-on-top-of-another-base)
      - [2.1.5.2. Abort a rebase](#2152-abort-a-rebase)
      - [2.1.5.3. Continue a rebase after resolving conflicts](#2153-continue-a-rebase-after-resolving-conflicts)
    - [2.1.6. Undo](#216-undo)
      - [2.1.6.1. Revert the changes in a commit and record them in a new commit](#2161-revert-the-changes-in-a-commit-and-record-them-in-a-new-commit)
      - [2.1.6.2. Reset to a previous commit and preserve the changes made since [commit] as unstaged](#2162-reset-to-a-previous-commit-and-preserve-the-changes-made-since-commit-as-unstaged)
      - [2.1.6.3. Reset to a previous commit and discard the changes made since the [commit]](#2163-reset-to-a-previous-commit-and-discard-the-changes-made-since-the-commit)
    - [2.1.7. Stash](#217-stash)
      - [2.1.7.1. Stash modified and staged changes](#2171-stash-modified-and-staged-changes)
      - [2.1.7.2. Stash modified and staged changes with a custom message](#2172-stash-modified-and-staged-changes-with-a-custom-message)
      - [2.1.7.3. Stash a selected file by specifying a path](#2173-stash-a-selected-file-by-specifying-a-path)
      - [2.1.7.4. List all stashed changesets](#2174-list-all-stashed-changesets)
      - [2.1.7.5. Restore the most recently stashed changeset and delete it](#2175-restore-the-most-recently-stashed-changeset-and-delete-it)
      - [2.1.7.6. Delete the most recently stashed changeset](#2176-delete-the-most-recently-stashed-changeset)
    - [2.1.8. Tags](#218-tags)
      - [2.1.8.1. Create a new tag](#2181-create-a-new-tag)
      - [2.1.8.2. List all tags](#2182-list-all-tags)
      - [2.1.8.3. Delete a tag](#2183-delete-a-tag)
    - [2.1.9. Repository Setup](#219-repository-setup)
      - [2.1.9.1. Create an empty repository in the current folder](#2191-create-an-empty-repository-in-the-current-folder)
      - [2.1.9.2. Create an empty repository in a specific folder](#2192-create-an-empty-repository-in-a-specific-folder)
      - [2.1.9.3. Clone a repository and add it to the current folder](#2193-clone-a-repository-and-add-it-to-the-current-folder)
      - [2.1.9.4. Clone a repository to a specific folder](#2194-clone-a-repository-to-a-specific-folder)
    - [2.1.10. Global Config](#2110-global-config)
      - [2.1.10.1. Set the username](#21101-set-the-username)
      - [2.1.10.2. Set the user email](#21102-set-the-user-email)
      - [2.1.10.3. Set automatic command line coloring](#21103-set-automatic-command-line-coloring)
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
  - [3.2. Usefull Functions](#32-usefull-functions)
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

#### 2.1.1.1. Display the status of modified files

`git status`

#### 2.1.1.2. Add a file to staging as it looks right now

`git add [file_name]`

#### 2.1.1.3. Add a folder to staging as it looks right now

`git add [folder_name]`

#### 2.1.1.4. Commit staged files in a new commit

`git commit -m "descriptive_message"`

#### 2.1.1.5. Add all files to staging and commit them at once

`git commit -am "descriptive_message"`

#### 2.1.1.6. Unstage a file while retaining the changes

`git reset [file_name]`

#### 2.1.1.7. Diff of what is changed but not staged

`git diff`

#### 2.1.1.8. Diff of what has changed between staged changes and the last commit

`git diff --staged`

### 2.1.2. Branches

#### 2.1.2.1. List all branches. The current one is marked with *

`git branch`

#### 2.1.2.2. Create a new branch

`git branch [branch_name]`

#### 2.1.2.3. Switch to a branch

`git checkout [branch_name]`

#### 2.1.2.4. Create a new branch and switch to it

`git checkout -b [branch_name]`

#### 2.1.2.5. Switch to the previously checked out branch

`git checkout -`

#### 2.1.2.6. Rename a branch

`git checkout -m [new_branch]`

#### 2.1.2.7. Delete a branch, locally

`git branch -d [branch_name]`

#### 2.1.2.8. Merge another branch into the current one

`git merge [branch_name]`

### 2.1.3. Working with a Remote Repository

#### 2.1.3.1. Fetch and merge all commits from the tracked remote branch

`git pull`

#### 2.1.3.2. Fetch and merge all commits from a specific remote branch

`git pull [alias] [branch_name]`

#### 2.1.3.3. Fetch recent changes from the tracked remote branch but don't merge them

`git fetch`

#### 2.1.3.4. Push all local branch commits to the tracked remote branch

`git push`

#### 2.1.3.5. Push all local branch commits to a specific remote branch

`git push [alias] [branch_name]`

#### 2.1.3.6. Add a new remote repository with the given alias

`git remote add [alias] [repo_url]`

#### 2.1.3.7. Display a list of remote repositories and their URLs

`git remote -v`

### 2.1.4. Commit History

#### 2.1.4.1. Show all commits in the current branch’s history

`git log`

#### 2.1.4.2. Show all commits in the current branch’s history by printing each commit on a single line

`git log --oneline`

#### 2.1.4.3. Show number of commits per author on all branches, excluding merge commits

`git shortlog -s -n --all --no-merges`

#### 2.1.4.4. Show number of commits per author on a branch, excluding merge commits

`git shortlog -s -n [branch_name] --no-merges`

#### 2.1.4.5. Show number of commits per author on all branches, including merge commits

`git shortlog -s -n --all`

#### 2.1.4.6. Show number of commits per author on a branch, including merge commits

`git shortlog -s -n [branch_name]`

### 2.1.5. Rebase

#### 2.1.5.1. Reapply commits from the current branch on top of another base

`git rebase [branch_name]`

#### 2.1.5.2. Abort a rebase

`git rebase –-abort`

#### 2.1.5.3. Continue a rebase after resolving conflicts

`git rebase –-continue`

### 2.1.6. Undo

#### 2.1.6.1. Revert the changes in a commit and record them in a new commit

`git revert [commit]`

#### 2.1.6.2. Reset to a previous commit and preserve the changes made since [commit] as unstaged

`git reset [commit]`

#### 2.1.6.3. Reset to a previous commit and discard the changes made since the [commit]

`git reset --hard [commit]`

### 2.1.7. Stash

#### 2.1.7.1. Stash modified and staged changes

`git stash`

#### 2.1.7.2. Stash modified and staged changes with a custom message

`git stash push -m "message"`

#### 2.1.7.3. Stash a selected file by specifying a path

`git stash push src/custom.css`

#### 2.1.7.4. List all stashed changesets

`git stash list`

#### 2.1.7.5. Restore the most recently stashed changeset and delete it

`git stash pop`

#### 2.1.7.6. Delete the most recently stashed changeset

`git stash drop`

### 2.1.8. Tags

#### 2.1.8.1. Create a new tag

`git tag "tagname"`

#### 2.1.8.2. List all tags

`git tag`

#### 2.1.8.3. Delete a tag

`git tag -d "tagname"`

### 2.1.9. Repository Setup

#### 2.1.9.1. Create an empty repository in the current folder

`git init`

#### 2.1.9.2. Create an empty repository in a specific folder

`git init [folder_name]`

#### 2.1.9.3. Clone a repository and add it to the current folder

`git clone [repo_url]`

#### 2.1.9.4. Clone a repository to a specific folder

`git clone [repo_url] [folder_name]`

### 2.1.10. Global Config

#### 2.1.10.1. Set the username

`git config --global user.name "user_name"`

#### 2.1.10.2. Set the user email

`git config --global user.email "user_email"`

#### 2.1.10.3. Set automatic command line coloring

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

## 3.2. Usefull Functions

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
