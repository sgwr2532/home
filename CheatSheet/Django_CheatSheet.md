## Django
~~~
# 基本的なコマンド
プロジェクト作成: django-admin startproject プロジェクト名
アプリケーション作成: python manage.py startapp アプリ名
開発サーバー起動: python manage.py runserver
マイグレーション作成: python manage.py makemigrations
データベースにマイグレーション適用: python manage.py migrate
管理ユーザー作成: python manage.py createsuperuser
~~~
#### テンプレート
~~~
# プロジェクト構造
プロジェクト名/
    manage.py
    プロジェクト名/
        __init__.py
        settings.py
        urls.py
        wsgi.py

# アプリケーション構造
アプリ名/
    __init__.py
    admin.py
    apps.py
    models.py
    tests.py
    views.py
    migrations/
        __init__.py

# 基本的なビュー
from django.http import HttpResponse
def index(request):
    return HttpResponse("Hello, world!")

# URL設定
from django.urls import path
from . import views

urlpatterns = [
    path('', views.index, name='index'),
]
~~~
