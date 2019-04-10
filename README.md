# QuickSnap-web
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
  启动浏览器，地址栏输入"http://localhost:5000" 并访问，即完成本web版微博的运行，如下图所示。
  ![avatar](https://github.com/Happyxianyueveryday/Computer-Vision-demo/blob/master/Demo_2/pics/QQ%E6%88%AA%E5%9B%BE20190410204225.png)
  
  ### Step 5：直接访问网址
  除了在本地构建和运行外，也可以直接访问该项目的网址，该项目由github进行托管： 
  
  ## 2. 基本功能
  本项目较为全面地实现了基本的微博功能，包括：
  
  + 用户账户注册，登录，登出
  + 编辑和发送微博
  + 基于whoosh的文档全局搜索
  + 关注，取消关注用户
  + 生成关注用户的微博动态
  
  本项目同样含有部分的功能尚待完成，即首页的推荐功能，该功能目前不可用，目前计划在下一个版本中结合个人在实验室的另一个项目——基于同态加密的分布式协同过滤系统进行更新。
  
 
  ## 3. 项目结构
  本项目的项目结构如下所示，需要注意的是，此处只展示了重要的源代码部分。
  
  
  
  ## 4. flask基本设计思想
  
  ### A. ORM的基本思想
  ORM
  
  ### B. MVC设计模式
  MVC是一种经典的web应用软件开发和组织思想。
  
  ![avatar](https://github.com/Happyxianyueveryday/Computer-Vision-demo/blob/master/Demo_2/pics/MVC.png)
  
  MVC中的V代表View，即视图层；C代表Controller，即控制器；M代表Model，即模型，是底层的数据库。三部分组件的基本功能如下。
  (1) 视图(View)：是指用户看到并与之交互的html界面，视图只负责如何显示从控制器得到的结果数据。
  (2) 控制器(Controller)：控制器接受用户的输入并调用模型中的视图去完成用户的需求，控制器本身不输出任何东西和做任何处理。它只是接收请求并决定调用哪个模型构件去处理请求，然后再确定用哪个视图来显示返回的数据。
  (3) 模型(Model)：模型表示业务规则，底层和数据库直接相连。在MVC的三个部件中，模型拥有最多的处理任务。被模型返回的数据是中立的，模型与数据格式无关，这样一个模型能为多个视图提供数据，由于应用于模型的代码只需写一次就可以被多个视图重用，所以减少了代码的重复性。
  
  ### C. flask的变形版MVC——MTV设计模式
  具体到flask后端框架，它使用的设计模式是MTV，这是一种变形版的MVC。
  
   ![avatar](https://github.com/Happyxianyueveryday/Computer-Vision-demo/blob/master/Demo_2/pics/MTV.png)
   
  MTV中的M代表模型(Models)，对应于这个项目中的'/app/model.py'文件；T代表模板(Templates)，对应于这个项目中的'app/templates/'文件夹；V代表视图(Views)，对应于这个项目中的'app/views.py'文件。另外还有一个额外的部件为控制器(Controller)，四个部分的具体功能如下所示。
  (1) 模型(Models)：
  (2) 模板(Templates)：
  (3) 视图(Views)：
  (4) 控制器(Controller)：
  
  
  具体到本项目，我们以删除一条已经发送的微博来展示整个flask架构的MTV设计模式是如何工作的，我们假设web应用仅在本机上运行，端口号为5000 (localhost:5000)：
  (1) 用户点击删除微博的按钮，发送一个url：'localhost:5000/delweibo/id=1'，这里的'/delweibo'指明了要删除功能，'/id=1'指定了要删除的微博的id
  (2) 控制器(Controller)的工作：根据用户点击时发送的url，匹配到视图view.py中的一个视图函数delweibo，将要删除的id作为参数传递给视图函数delweibo。
  (3) 视图(View)的工作：视图部分做最多的处理工作，在视图中的视图函数delweibo被调用后，需要首先检查删除操作的合法性（
  (4) 模型(Model)的工作：
  (5) 模板(Templates)的工作：
 
  
  ## 5. 安全性策略
  
  本项目中的安全性主要分为三个部分：密码安全性，url安全性，表单安全性。
  
  ### A. 密码安全性
  
  ### B. url安全性
  
  ### C. 表单安全性
  
  
  
  
  
  
