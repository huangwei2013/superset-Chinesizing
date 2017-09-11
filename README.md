Superset搭配Druid很好，可是汉化不够给力，还是需要自己搬点砖

##0.基本设定
  python2.7 &  安装目录为 /usr/local/lib/python2.7/
  
1.基本汉化(来自常见教程)

编辑/usr/local/lib/python2.7/dist-packages/superset/config.py

    将
        BABEL_DEFAULT_LOCALE  指向中文

下载语言包(有时这个语言包已经下载好了，可跳过这一步)

    https://github.com/ApacheInfra/superset/blob/master/superset/translations/zh/LC_MESSAGES/messages.po
    下载完成后，将文件放在下面的目录下
    /usr/local/lib/python2.7/dist-packages/flask_appbuilder/translations/zh/LC_MESSAGES/messages.po


编译语言包

    在 /usr/local/lib/python2.7/dist-packages/flask_appbuilder/ 目录下执行
        pybabel compile -d translations
        

##2.更进一步（的苦力活）

编辑/usr/local/lib/python2.7/dist-packages/superset/config.py

    将
        BABEL_DEFAULT_LOCALE  指向中文

直接修改汉化文件内容
     /usr/local/lib/python2.7/dist-packages /flask_appbuilder/translations/zh/LC_MESSAGES/
     下的 messages.po （对应有一个 messages.mo），用poEdit等编辑器编辑 po 文件

     Note：
          编辑的内容和代码文件+行数有关，不同版本应该无法通用

