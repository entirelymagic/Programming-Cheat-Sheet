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
- [7. Operating Systems](#7-operating-systems)
  - [7.1. Linux](#71-linux)
    - [7.1.1. Files and Navigating](#711-files-and-navigating)
      - [7.1.1.1. Directory listening](#7111-directory-listening)
      - [7.1.1.2. Formatted listening](#7112-formatted-listening)
      - [7.1.1.3. Formatted listening including hidden files](#7113-formatted-listening-including-hidden-files)
      - [7.1.1.4. Change directory](#7114-change-directory)
      - [7.1.1.5. Change to parent directory](#7115-change-to-parent-directory)
      - [7.1.1.6. Show the path where actually you are](#7116-show-the-path-where-actually-you-are)
      - [7.1.1.7. Create a directory](#7117-create-a-directory)
      - [7.1.1.8. Remove directory](#7118-remove-directory)
      - [7.1.1.9. Force remove](#7119-force-remove)
      - [7.1.1.10. file](#71110-file)
      - [7.1.1.11. Rename or moove file](#71111-rename-or-moove-file)
      - [7.1.1.12. Create file](#71112-create-file)
      - [7.1.1.13. Output contents of file](#71113-output-contents-of-file)
      - [7.1.1.14. Write standart input into file](#71114-write-standart-input-into-file)
      - [7.1.1.15. Append standart input into file](#71115-append-standart-input-into-file)
      - [7.1.1.16. Output contents of file it grows](#71116-output-contents-of-file-it-grows)
    - [7.1.2. Networking](#712-networking)
      - [7.1.2.1. Ping host](#7121-ping-host)
      - [7.1.2.2. Show the actually routing table](#7122-show-the-actually-routing-table)
      - [7.1.2.3. Check your iptable's rules](#7123-check-your-iptables-rules)
      - [7.1.2.4. List all ports](#7124-list-all-ports)
      - [7.1.2.5. Got whois for domain](#7125-got-whois-for-domain)
      - [7.1.2.6. Get DNS for domain](#7126-get-dns-for-domain)
      - [7.1.2.7. Reserve lookup host](#7127-reserve-lookup-host)
      - [7.1.2.8. Download file](#7128-download-file)
      - [7.1.2.9. Recurively download files from url](#7129-recurively-download-files-from-url)
      - [7.1.2.10. Outputs the webpage from url](#71210-outputs-the-webpage-from-url)
      - [7.1.2.11. Connect to host as user](#71211-connect-to-host-as-user)
      - [7.1.2.12. Connect using port](#71212-connect-using-port)
      - [7.1.2.13. Connect and use bind port](#71213-connect-and-use-bind-port)
    - [7.1.3. Processes](#713-processes)
      - [7.1.3.1. Display currently active processes](#7131-display-currently-active-processes)
      - [7.1.3.2. Detailed outputs](#7132-detailed-outputs)
      - [7.1.3.3. Kill process with process id (pid)](#7133-kill-process-with-process-id-pid)
      - [7.1.3.4. Kill all processes named proc](#7134-kill-all-processes-named-proc)
    - [7.1.4. System Info](#714-system-info)
      - [7.1.4.1. Show current date/time](#7141-show-current-datetime)
      - [7.1.4.2. Show uptime](#7142-show-uptime)
      - [7.1.4.3. Who you're logged in as](#7143-who-youre-logged-in-as)
      - [7.1.4.4. Display who is online](#7144-display-who-is-online)
      - [7.1.4.5. Memory info](#7145-memory-info)
      - [7.1.4.6. Show memory and swap usage](#7146-show-memory-and-swap-usage)
      - [7.1.4.7. Show directory space usage](#7147-show-directory-space-usage)
      - [7.1.4.8. Displays readable size in GB](#7148-displays-readable-size-in-gb)
      - [7.1.4.9. Show disk usage](#7149-show-disk-usage)
      - [7.1.4.10. Show karnel config](#71410-show-karnel-config)
    - [7.1.5. Compressing](#715-compressing)
      - [7.1.5.1. Tar files into file.tar](#7151-tar-files-into-filetar)
      - [7.1.5.2. Untar into current directory](#7152-untar-into-current-directory)
      - [7.1.5.3. Show contents of archive](#7153-show-contents-of-archive)
    - [7.1.6. Permissions](#716-permissions)
      - [7.1.6.1. Change permissions of file](#7161-change-permissions-of-file)
    - [7.1.7. Others](#717-others)
      - [7.1.7.1. Search in files for pattern](#7171-search-in-files-for-pattern)
      - [7.1.7.2. Search for pattern recursively in dir](#7172-search-for-pattern-recursively-in-dir)
      - [7.1.7.3. Find all instances of file](#7173-find-all-instances-of-file)
      - [7.1.7.4. Show possible locations of app](#7174-show-possible-locations-of-app)
- [Resources](#resources)

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

# 7. Operating Systems

## 7.1. Linux

### 7.1.1. Files and Navigating

#### 7.1.1.1. Directory listening

`ls`

#### 7.1.1.2. Formatted listening

`ls -l`

#### 7.1.1.3. Formatted listening including hidden files

`ls -la`

#### 7.1.1.4. Change directory

`cd`

#### 7.1.1.5. Change to parent directory

`cd..`

#### 7.1.1.6. Show the path where actually you are

`pwd`

#### 7.1.1.7. Create a directory

`mkdir`

#### 7.1.1.8. Remove directory

`rm -r`

#### 7.1.1.9. Force remove

`rm -f`

#### 7.1.1.10. file

`cp`

#### 7.1.1.11. Rename or moove file

`mv`

#### 7.1.1.12. Create file

`touch file`

#### 7.1.1.13. Output contents of file

`cat [file]`

#### 7.1.1.14. Write standart input into file

`cat > [file]`

#### 7.1.1.15. Append standart input into file

`cat >> [file]`

#### 7.1.1.16. Output contents of file it grows

`tail -f [file]`

### 7.1.2. Networking

#### 7.1.2.1. Ping host

`ping [host]`

#### 7.1.2.2. Show the actually routing table

`route -n`

#### 7.1.2.3. Check your iptable's rules

`iptables -L`

#### 7.1.2.4. List all ports

`netstat -a`

#### 7.1.2.5. Got whois for domain

`whois [domain]`

#### 7.1.2.6. Get DNS for domain

`dig [domain]`

#### 7.1.2.7. Reserve lookup host

`dig -x [host]`

#### 7.1.2.8. Download file

`wget [file]`

#### 7.1.2.9. Recurively download files from url

`wget -r [url]`

#### 7.1.2.10. Outputs the webpage from url

`curl [url]`

#### 7.1.2.11. Connect to host as user

`ssh user@host`

#### 7.1.2.12. Connect using port

`ssh -p [port] user@host`

#### 7.1.2.13. Connect and use bind port

`ssh -D user@host`

### 7.1.3. Processes

#### 7.1.3.1. Display currently active processes

`ps`

#### 7.1.3.2. Detailed outputs

`ps -aux`

#### 7.1.3.3. Kill process with process id (pid)

`kill [pid]`

#### 7.1.3.4. Kill all processes named proc

`killall proc`

### 7.1.4. System Info

#### 7.1.4.1. Show current date/time

`date`

#### 7.1.4.2. Show uptime

`uptime`

#### 7.1.4.3. Who you're logged in as

`whoami`

#### 7.1.4.4. Display who is online

`w`

Display cpu info

`cat /proc/cpuinfo`

#### 7.1.4.5. Memory info

`cat /proc/meminfo`

#### 7.1.4.6. Show memory and swap usage

`free`

#### 7.1.4.7. Show directory space usage

`du`

#### 7.1.4.8. Displays readable size in GB

`du -sh`

#### 7.1.4.9. Show disk usage

`df`

#### 7.1.4.10. Show karnel config

`uname -a`

### 7.1.5. Compressing

#### 7.1.5.1. Tar files into file.tar

`tar -cf [file.tar] [files]`

#### 7.1.5.2. Untar into current directory

`tar -xf [file.tar]`

#### 7.1.5.3. Show contents of archive

Show contents of archive
Options :

- c - create archive
-
- t - table of contents
-
- x - extract
-
- z - use zip/gzip
-
- f - specify filename
-
- k - do not overwrite
-
- v - verbose

### 7.1.6. Permissions

#### 7.1.6.1. Change permissions of file

`chmod [rights] [file]`

4 - read(r)

2 - write(w)

1 - execute(x)

> order : owner / group / world

`chmod 777` - rwx for everyone

`chmod 755` - rw for owner, rx for group and world

### 7.1.7. Others

#### 7.1.7.1. Search in files for pattern

`grep '[pattern]' [files]`

#### 7.1.7.2. Search for pattern recursively in dir

`grep -r '[pattern]' dir`

#### 7.1.7.3. Find all instances of file

`locate [file]`

#### 7.1.7.4. Show possible locations of app

`whereis [app]`

# Resources

There will be added more resources in the future.

- Linux Cheatsheet from Visual studio Code

-
