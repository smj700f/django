# 建立 Django 虛擬環境
- [建立Django虛擬環境](#建置Django虛擬環境)
- [進入Django虛擬環境](#進入Django虛擬環境)
- [安裝django](#安裝django)
- [查看django相關訊息](#查看django相關訊息)
- [更新django](#更新django)
- [查看Django環境有哪些套件](#查看Django環境有哪些套件)
# 建立 Django 專案
- [切入根目錄路徑](#切入根目錄路徑)
- [建立example資料夾](#建立example資料夾)
- [切入example資料夾](#切入example資料夾)
- [建立firstproject專案資料夾](#建立firstproject專案資料夾)
- [顯示firstproject有哪些項目](#顯示firstproject有哪些項目)
- [顯示firstproject樹狀目錄](#顯示firstproject樹狀目錄)
- [切入example資料夾](#切入example資料夾)
- [建立Application應用程式](#建立Application應用程式)
- [啟動伺服器](#啟動伺服器)
- [建立templates目錄](#建立templates目錄)
- [建立static目錄](#建立static目錄)
- [將模型同步到資料庫](#將模型同步到資料庫)

## 建置Django虛擬環境
```
conda create -n Django python=3.6 -y

```
## 進入Django虛擬環境
```
conda activate django

```
## 安裝django
```
pip install django

```
## 查看django相關訊息
```
pip show django

```
#### 輸出：
```
Name: Django
Version: 3.2.13
Summary: A high-level Python Web framework that encourages rapid development and clean, pragmatic design.
Home-page: https://www.djangoproject.com/
Author: Django Software Foundation
Author-email: foundation@djangoproject.com
License: BSD-3-Clause
Location: c:\users\d4071\miniconda3\envs\django\lib\site-packages
Requires: asgiref, pytz, sqlparse
Required-by:
```
## 更新django
```
pip install -U Django

```
## 查看Django環境有哪些模組
```
pip list

```
#### 輸出：
```
Package           Version
----------------- ---------
asgiref           3.4.1
certifi           2020.6.20
Django            3.2.13
pip               21.2.2
pytz              2022.1
setuptools        58.0.4
sqlparse          0.4.2
typing_extensions 4.1.1
wheel             0.37.1
wincertstore      0.2
```
## 切入根目錄路徑
```
cd \

```
## 建立example資料夾
```
mkdir example

```
## 切入example資料夾
```
cd example

```
## 建立firstproject專案資料夾
```
django-admin startproject firstproject

```
## 顯示firstproject有哪些項目
```
dir firstproject

```
#### 輸出：
```
 磁碟區 C 中的磁碟是 Acer
 磁碟區序號:  CC30-03FC

 C:\example\firstproject 的目錄

2022/05/06  上午 07:27    <DIR>          .
2022/05/06  上午 07:27    <DIR>          ..
2022/05/06  上午 07:27    <DIR>          firstproject
2022/05/06  上午 07:27               690 manage.py
               1 個檔案             690 位元組
               3 個目錄  250,895,433,728 位元組可用
```
## 顯示firstproject樹狀目錄
```
tree /f

```
#### 輸出：
```
列出磁碟區 Acer 的資料夾 PATH
磁碟區序號為 CC30-03FC
C:.
└─firstproject
    │  manage.py
    │
    └─firstproject
            asgi.py
            settings.py
            urls.py
            wsgi.py
            __init__.py
```
## 切入example資料夾
```
cd firstproject

```
## 建立Application應用程式
```
python manage.py startapp myapp

```
#### 輸出：
```
列出磁碟區 Acer 的資料夾 PATH
磁碟區序號為 CC30-03FC
C:.
│  manage.py
│
├─firstproject
│  │  asgi.py
│  │  settings.py
│  │  urls.py
│  │  wsgi.py
│  │  __init__.py
│  │
│  └─__pycache__
│          settings.cpython-36.pyc
│          __init__.cpython-36.pyc
│
└─myapp
    │  admin.py
    │  apps.py
    │  models.py
    │  tests.py
    │  views.py
    │  __init__.py
    │
    └─migrations
            __init__.py
```
## 啟動伺服器
```
python manage.py runserver

```
#### 輸出：
```
Watching for file changes with StatReloader
Performing system checks...

System check identified no issues (0 silenced).

You have 18 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
Run 'python manage.py migrate' to apply them.
May 06, 2022 - 07:48:19
Django version 3.2.13, using settings 'firstproject.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CTRL-BREAK.
[06/May/2022 07:48:55] "GET / HTTP/1.1" 200 10697
[06/May/2022 07:48:55] "GET /static/admin/css/fonts.css HTTP/1.1" 200 423
[06/May/2022 07:48:56] "GET /static/admin/fonts/Roboto-Regular-webfont.woff HTTP/1.1" 200 85876
[06/May/2022 07:48:56] "GET /static/admin/fonts/Roboto-Bold-webfont.woff HTTP/1.1" 200 86184
[06/May/2022 07:48:56] "GET /static/admin/fonts/Roboto-Light-webfont.woff HTTP/1.1" 200 85692
Not Found: /favicon.ico
[06/May/2022 07:48:56] "GET /favicon.ico HTTP/1.1" 404 2116
[06/May/2022 07:49:54] "GET / HTTP/1.1" 200 10697
```
#### `firstproject.setting` 為環境的設定檔
#### `http://127.0.0.1:8000/` 為開啟伺服器網址

## 建立templates目錄
```
md templates

```
#### 輸出：
```
列出磁碟區 Acer 的資料夾 PATH
磁碟區序號為 CC30-03FC
C:.
│  db.sqlite3
│  manage.py
│
├─firstproject
│  │  asgi.py
│  │  settings.py
│  │  urls.py
│  │  wsgi.py
│  │  __init__.py
│  │
│  └─__pycache__
│          settings.cpython-36.pyc
│          urls.cpython-36.pyc
│          wsgi.cpython-36.pyc
│          __init__.cpython-36.pyc
│
├─myapp
│  │  admin.py
│  │  apps.py
│  │  models.py
│  │  tests.py
│  │  views.py
│  │  __init__.py
│  │
│  └─migrations
│          __init__.py
│
└─templates
```
## 建立static目錄
```
md static

```
#### 輸出：
```
列出磁碟區 Acer 的資料夾 PATH
磁碟區序號為 CC30-03FC
C:.
│  db.sqlite3
│  manage.py
│
├─firstproject
│  │  asgi.py
│  │  settings.py
│  │  urls.py
│  │  wsgi.py
│  │  __init__.py
│  │
│  └─__pycache__
│          settings.cpython-36.pyc
│          urls.cpython-36.pyc
│          wsgi.cpython-36.pyc
│          __init__.cpython-36.pyc
│
├─myapp
│  │  admin.py
│  │  apps.py
│  │  models.py
│  │  tests.py
│  │  views.py
│  │  __init__.py
│  │
│  └─migrations
│          __init__.py
│
├─static
└─templates
```
## 將模型同步到資料庫
#### 資料庫檔案位置：`C:\example\firstproject\db.sqlite3`
```
python manage.py migrate

```
```
Operations to perform:
  Apply all migrations: admin, auth, contenttypes, sessions
Running migrations:
  Applying contenttypes.0001_initial... OK
  Applying auth.0001_initial... OK
  Applying admin.0001_initial... OK
  Applying admin.0002_logentry_remove_auto_add... OK
  Applying admin.0003_logentry_add_action_flag_choices... OK
  Applying contenttypes.0002_remove_content_type_name... OK
  Applying auth.0002_alter_permission_name_max_length... OK
  Applying auth.0003_alter_user_email_max_length... OK
  Applying auth.0004_alter_user_username_opts... OK
  Applying auth.0005_alter_user_last_login_null... OK
  Applying auth.0006_require_contenttypes_0002... OK
  Applying auth.0007_alter_validators_add_error_messages... OK
  Applying auth.0008_alter_user_username_max_length... OK
  Applying auth.0009_alter_user_last_name_max_length... OK
  Applying auth.0010_alter_group_name_max_length... OK
  Applying auth.0011_update_proxy_permissions... OK
  Applying auth.0012_alter_user_first_name_max_length... OK
  Applying sessions.0001_initial... OK
  #### 輸出：
```
