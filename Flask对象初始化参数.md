# Flask对象的初始化参数

 Flask程序实例在创建的时候,需要默认传入当前Flask程序所指定的包(模块)

-  import_name 

  -  Flask程序所在的包(模块),传  __ name __就可以 (--name--中间是没有空格的，这里是会涉及到加粗属性)

  -  可以决定Flask在访问静态文件时查找的路径 

    【这个就类似于Django里面的setting.py里面的要去添加的模块或者静态文件，然后让它识别（图片可以放在静态文件里面，然后输入网址   127.0.0.1:5000/static/img.png  这里面的static就是存放静态文件的地方，同理还有模块templates）】

-   static_url_path 

  -  静态文件**访问路径**,可以不传,默认为: /+static_folder 

    改静态文件访问路径的名字 如把 静态文件 static 改成  test 那么网址的  **路径**  就会是127.0.0.1:5000/test/img.png

    ````bask
    app = Flask(__name__,static_url_path='/test')
    ````

-   static_folder 

  -  静态文件存储的文件夹,可以不传,默认为 static （这个是文件名，不是路径！）

    ````bask
    app = Flask(__name__,static_url_path='/test',  static_folder='test')
    ````

    注意：这里的static_folder='test' 旁边的文件夹的名字也要重命名成test不然识别不出来。

-  template _folder
  -  模板文件存储的文件夹,可以不传,默认为  templates （这个是文件名，不是路径！）