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
# 環境設定
- [DEBUG除錯模式設定](#DEBUG除錯模式設定)
- [加入Application應用程式](#加入Application應用程式)
- [設定Template路徑](#設定Template路徑)
- [設定static靜態檔路徑](#設定static靜態檔路徑)
- [設定中文語系和時區](#設定中文語系和時區)
- [開始寫網頁sayhello](#開始寫網頁sayhello)
- [網址傳送參數，顯示網頁](#網址傳送參數，顯示網頁)
- [模板的使用](#模板的使用)
- [加入靜態檔案](#加入靜態檔案)

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
## DEBUG除錯模式設定
#### `settings.py`檔案路徑位置：`C:\example\firstproject\firstproject\settings.py`
### 啟動伺服器上線之前，開啟`settings.py`，將`DEBUG`模式設定為`False`
```
DEBUG = False

```
### 下線之後，開啟`settings.py`，將`DEBUG`模式設定為`True`
```
DEBUG = True

```
## 加入Application應用程式
#### `settings.py`檔案路徑位置：`C:\example\firstproject\firstproject\settings.py`
### 開啟`settings.py`，找到以下位置
```
# Application definition

INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
]

```
### 加入`'myapp', #新增的app`後，儲存`settings.py`
```
# Application definition

INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'myapp', #新增的app
]

```
## 設定Template路徑
#### `settings.py`檔案路徑位置：`C:\example\firstproject\firstproject\settings.py`
### 開啟`settings.py`，找到以下位置
```
TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [],
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                'django.template.context_processors.debug',
                'django.template.context_processors.request',
                'django.contrib.auth.context_processors.auth',
                'django.contrib.messages.context_processors.messages',
            ],
        },
    },
]

```
### 在`'DIRS': []`中,加入`BASE_DIR / 'templates'`後，儲存`settings.py`
```
TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [BASE_DIR / 'templates'],
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                'django.template.context_processors.debug',
                'django.template.context_processors.request',
                'django.contrib.auth.context_processors.auth',
                'django.contrib.messages.context_processors.messages',
            ],
        },
    },
]

```
## 設定static靜態檔路徑
#### `settings.py`檔案路徑位置：`C:\example\firstproject\firstproject\settings.py`
### 開啟`settings.py`，找到以下位置
```
STATIC_URL = '/static/'

```
### 加入以下路徑後，儲存`settings.py`
```
STATIC_URL = '/static/'
STATICFILES_DIRS = [
    BASE_DIR / 'static' #加入static路徑
]

```
## 設定中文語系和時區
#### `settings.py`檔案路徑位置：`C:\example\firstproject\firstproject\settings.py`
### 開啟`settings.py`，找到以下位置
```
# Internationalization
# https://docs.djangoproject.com/en/3.2/topics/i18n/

LANGUAGE_CODE = 'en-us'

TIME_ZONE = 'UTC'

USE_I18N = True

USE_L10N = True

USE_TZ = True

```
### 設定以下配置後，儲存`settings.py`
```
# Internationalization
# https://docs.djangoproject.com/en/3.2/topics/i18n/

LANGUAGE_CODE = 'zh-hant'

TIME_ZONE = 'Asia/Taipei'

USE_I18N = True

USE_L10N = True

USE_TZ = True

```
## 開始寫網頁sayhello
#### `urls.py`檔案路徑位置：`C:\example\firstproject\firstproject\urls.py`
### 開啟`urls.py`
```
from django.contrib import admin
from django.urls import path

urlpatterns = [
    path('admin/', admin.site.urls),
]

```
### 加入HttpResponse模組，sayhello函數，呼叫sayhello函數後，儲存`settings.py`
```
from django.contrib import admin
from django.urls import path
from django.http import HttpResponse

def sayhello(request):
    return HttpResponse("Hello Django！")

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', sayhello),
]

```
#### 設定完成後在 瀏覽器輸入`http://127.0.0.1:8000/`，或F5鍵重新整理網頁

## 網址傳送參數，顯示網頁
#### `urls.py`檔案路徑位置：`C:\example\firstproject\firstproject\urls.py`
### 開啟`urls.py`
```
from django.contrib import admin
from django.urls import path
from django.http import HttpResponse

def sayhello(request):
    return HttpResponse("Hello Django！")

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', sayhello),
]

```
### 加入以下hello2函數及呼叫hello2，儲存`settings.py`
```
from django.contrib import admin
from django.urls import path
from django.http import HttpResponse

def sayhello(request):
    return HttpResponse("Hello Django！")

def hello2(request, username):
    return HttpResponse("Hello " + username)

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', sayhello),
    path('hello2/<str:username>', hello2),
]

```
#### 設定完成後在 瀏覽器輸入`http://127.0.0.1:8000/hello2/username`，或F5鍵重新整理網頁
#### `username`是你個人電腦的使用者名稱，例如`d4071`

## 模板的使用
#### 在`C:\example\firstproject\templates`路徑中，新增hello3.html檔案
### 加入以下程式碼
```
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>第一個模板</title>
</head>
<body>
    <h1> 歡迎光臨：{{username}} </h1>
    <h2> 現在時刻：{{now}} </h2>
</body>
</html>

```
#### 在`C:\example\firstproject\myapp\views.py`路徑中，開啟`views.py`
### 加入datetime模組，hello3函數
```
from django.shortcuts import render
from datetime import datetime
# Create your views here.
def hello3(request, username):
    now = datetime.now()
    return render(request, "hello3.html", locals())

```
#### 在`"C:\example\firstproject\firstproject\urls.py"`路徑中，開啟`urls.py`
### 加入hello3函數，呼叫hello3函數
```
from django.contrib import admin
from django.urls import path
from django.http import HttpResponse
from myapp.views import hello3

def sayhello(request):
    return HttpResponse("Hello Django！")

def hello2(request, username):
    return HttpResponse("Hello " + username)

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', sayhello),
    path('hello2/<str:username>', hello2),
    path('hello3/<str:username>', hello3),
]
```
#### 設定完成後在 瀏覽器輸入`http://127.0.0.1:8000/hello3/username`，或F5鍵重新整理網頁
#### `username`是你個人電腦的使用者名稱，例如`d4071`

## 加入靜態檔案
#### 在`C:\example\firstproject\static`路徑中，新增css資料夾
#### 在`C:\example\firstproject\static\css`路徑中，新增style.css檔案
### 開啟`style.css`後，加入以下程式碼
```
.info {
    color:red;
    font-size: 1.5em;
}

```
#### 在`C:\example\firstproject\static`路徑中，新增images資料夾
#### 在`C:\example\firstproject\static\images`路徑中，加入圖片檔後，命名為`ball.png`
- [圖片檔範例下載](https://pngimg.com/uploads/football/football_PNG52797.png)

#### 在`C:\example\firstproject\templates`路徑中，新增hello4.html檔案
### 開啟`hello4.html`後，加入以下程式碼
```
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>第一個模板</title>
    {% load static %}
    <link href="{% static 'css/style.css' %}" rel="stylesheet" type="text/css" />
</head>
<body>
    <div id="home">
        <img src="{% static 'images/ball.png' %}" alt="歡迎光臨：" width="32" height="32" />
        <span class="info"> 歡迎光臨：{{username}} </span>
        <h2> 現在時刻：{{now}} </h2>
    </div>
</body>
</html>

```

#### 在`C:\example\firstproject\myapp\views.py`路徑中，開啟`views.py`
### 加入datetime模組，hello4函數
```
from django.shortcuts import render
from datetime import datetime
# Create your views here.
def hello3(request, username):
    now = datetime.now()
    return render(request, "hello3.html", locals())

def hello4(request, username):
    now = datetime.now()
    return render(request, "hello4.html", locals())
```
#### 在`"C:\example\firstproject\firstproject\urls.py"`路徑中，開啟`urls.py`
### 加入hello4函數，呼叫hello4函數
```
from django.contrib import admin
from django.urls import path
from django.http import HttpResponse
from myapp.views import hello3, hello4

def sayhello(request):
    return HttpResponse("Hello Django！")

def hello2(request, username):
    return HttpResponse("Hello " + username)

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', sayhello),
    path('hello2/<str:username>', hello2),
    path('hello3/<str:username>', hello3),
    path('hello4/<str:username>', hello4),
]
```
