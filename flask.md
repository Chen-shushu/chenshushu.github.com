# 安装

__运行虚拟机，在里面安装flask__

## 先创建一个虚拟环境

````bask
[qw@localhost ~]$ mkdir myproject
[qw@localhost ~]$ cd myproject
[qw@localhost myproject]$ python3 -m venv venv
````

###  激活虚拟环境

````bask
qw@localhost myproject]$ . venv/bin/activate
````

### 安装FLASK

````bask
(venv) [qw@localhost myproject]$ pip install Flask
````

### 来一个项目

````bask
from flask import Flask   #导入flask类

app = Flask(__name__)    #Flask类接收一个参改__name__

# 装饰器的作用是将路由映射到视图函数index
@app.route("/")         
def hello_world():      #Flask应用程序实例的run方法启动WEB服务器
    return "<p>Hello, World!</p>"

````

 ![第一个项目](C:\Users\Lenovo\Desktop\第一个项目.jpg)

![1626869214943](C:\Users\Lenovo\AppData\Roaming\Typora\typora-user-images\1626869214943.png)

**这个是在pycharm里面做的，要记得安装pycharm。**

**我是在pycharm里面新建了一个flask的项目。**

