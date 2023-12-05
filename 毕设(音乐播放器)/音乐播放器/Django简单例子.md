创建项目  
django-admin startproject [proj]  
  
```注册和配置app  
# 创建一个app（app指的是一个模块）  
python mamage.py startapp [app]  
  
# 在 [proj]/settings.py 下修改：  
INSTALLED_APPS = [  
    ...,  
    'app',  
]  
  
# 在 [app]/models.py 下创建模型类，如 MyModel  
  
# 迁移数据库  
python manage.py makemigrations  
python manage.py migrate  
  
# 在 [app]/views.py（二级路由）下创建视图  
from django.shortcuts import render  
from django.http import HttpResponse  
  
def my_view(request):  
    return HttpResponse('Hello,world!')  
  
# 在 [proj]/urls.py（一级路由）下添加路由  
from django.contrib import admin  
from django.urls import path  
from app import views  
  
urlpatterns = [  
    path('admin/', admin.site.urls),  
    path('myview/', views.my_view),  
]  
```  
  
```运行，访问  
python manage.py runserver 8000  
  
浏览器访问 http://localhost:8000/myview/  
```