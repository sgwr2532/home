## Django
~~~
# 基本的なコマンド
プロジェクト作成:			django-admin startproject プロジェクト名
アプリケーション作成:			python manage.py startapp アプリ名
開発サーバー起動:			python manage.py runserver
マイグレーション作成:			python manage.py makemigrations
データベースにマイグレーション適用:	python manage.py migrate
管理ユーザー作成: 			python manage.py createsuperuser
~~~
#### テンプレート
~~~
# プロジェクト構造
project
 |- manage.py
 |- project
 |   |- __init__.py
 |   |- asgi.py
 |   |- settings.py
 |   |- urls.py
 |   |- wsgi.py
 |- application
     |- migrations
     |   |- __init__.py
     |- __init__.py
     |- admin.py
     |- apps.py
     |- forms.py
     |- models.py
     |- tests.py
     |- urls.py
     |- views.py

# 基本的なビュー
from django.http import HttpResponse
def index(request):
    return HttpResponse("Hello, world!")

# project/urls.py 
from django.contrib import admin
from django.urls import path, views
urlpatterns = [
    path('', views.index, name='index'),
    path('admin/', admin.site.urls),
    path('application/', include('application.urls')),
]

# application/urls.py 
from django.urls import path
from . import views
app_name = 'application'
urlpatterns = [
  path('', views.IndexView.as_view(), name='index'),
  path('hoge/', views.HogeView.as_view(), name='hoge'),
]

~~~
