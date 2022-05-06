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
## 更新django
```
pip install -U Django

```
## 查看Django環境有哪些套件
```
pip list

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
## 顯示firstproject樹狀目錄
```
tree /f

```
## 切入example資料夾
```
cd firstproject

```
## 建立Application應用程式
```
python manage.py startapp myapp

```
## 啟動伺服器
```
python manage.py runserver

```
#### `firstproject.setting` 為環境的設定檔
#### `http://127.0.0.1:8000/` 為開啟伺服器網址

## 建立templates目錄
```
md templates

```
## 建立static目錄
```
md static

```
## 將模型同步到資料庫
#### 資料庫檔案位置：`C:\example\firstproject\db.sqlite3`
```
python manage.py migrate

```
