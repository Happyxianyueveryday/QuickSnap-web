# quicksnap-web
基于flask的简易微博web应用

## 1. 构建和运行
  ### Step 1：安装本项目所依赖的库：
  本项目主要基于flask实现后端，使用HTML和扩展UI库bootstrap实现前端。项目本身的运行和部署需要使用下面的第三方库。
  
  ```
  $ pip install flask
  $ pip install flask-login
  $ pip install flask-openid
  $ pip install flask-sqlalchemy
  $ pip install sqlalchemy-migrate
  $ pip install flask-wtf
  $ pip install flask-babel
  $ pip install guess_language
  $ pip install flipflop
  $ pip install coverage
  ```
  
  ### Step 2：下载本项目文件
  点击本页面右上角的"Clone or Download" 按钮，下载本项目，也可以按照个人喜好使用git工具进行clone到本地。
  
  ### Step 3：在项目下载的路径下直接运行
  在下载的本项目的本地路径下运行run.py脚本。
  
  ```
  $ python run.py
  ```
  
  ### Step 4: 启动任意浏览器访问本机
  启动浏览器，地址栏输入"http://localhost:5000" 并访问，即完成本web版微博的运行。
  
  
  ## 2. 基本功能
  本项目较为全面地实现了基本的微博功能，包括：
  
  + 用户账户注册，登录，登出，保存登录状态（记住我功能）
  + 编辑和发送微博
  + 基于whoosh的文档全局搜索
  + 关注，取消关注用户
  + 生成关注用户的微博动态
  
  本项目同样含有部分的功能尚待完成，即首页的推荐功能。前端使用Vue，同时具有移动端和pc端两份版本。
  
  pc端主页面：
  
  ![avatar](https://github.com/Happyxianyueveryday/Computer-Vision-demo/blob/master/Demo_2/pics/QQ%E6%88%AA%E5%9B%BE20190410204225.png)
  
  移动端主页面和微博内容页面：  
  
  ![avatar](https://github.com/Happyxianyueveryday/quicksnap-web/blob/master/pics/QQ%E6%88%AA%E5%9B%BE20190914005037.png)
  ![avatar](https://github.com/Happyxianyueveryday/quicksnap-web/blob/master/pics/QQ%E6%88%AA%E5%9B%BE20190914005119.png)
  
  
  
 
  ## 3. 项目结构
  本项目的项目结构如下所示，需要注意的是，此处只展示了重要的源代码部分。
  
  ```
  / -- |-- db_create.py: 数据库新建脚本
       |-- db_migrate.py: 数据库迁移脚本（使用方法：先迁移后更新）
       |-- db_update.py: 数据库更新脚本（使用方法：先迁移后更新）
       |-- config.py: 项目配置文件
       |-- run.py: 可执行脚本文件，直接执行该文件即可运行本项目
       |-- app --|
                 |-- __init__.py: 初始化文件
                 |-- forms.py: flask表单文件
                 |-- models.py: flask模型文件
                 |-- view.py: flask视图层文件
  ```
  
  
  
  
  
  
  
  
