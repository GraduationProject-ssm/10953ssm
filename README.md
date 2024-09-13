# [首页查询更多项目](https://github.com/GraduationProject-ssm) 包安装运行


# 10953ssm高校信息资源共享平台

![picture](https://raw.githubusercontent.com/GraduationProject-springboot/.github/main/img/wx.png)

### 点击播放视频 ▼
[![Watch the video](https://i.sstatic.net/Vp2cE.png)](https://www.bilibili.com/video/BV1Sh44eDEx6?p=53)


# 系统概述
进过系统的分析后，就开始记性系统的设计，系统设计包含总体设计和详细设计。总体设计只是一个大体的设计，经过了总体设计，我们能够划分出系统的一些东西，例如文件、文档、数据等。而且我们通过总体设计，大致可以划分出了程序的模块，以及功能。但是只是一个初步的分类，并没有真正的实现。

整体设计，只是一个初步设计，而且，对于一个项目，我们可以进行多个整体设计，通过对比，包括性能的对比、成本的对比、效益的对比，来最终确定一个最优的设计方案，选择优秀的整体设计可以降低开发成本，增加公司效益，从这一点来讲，整体设计还是非常重要的。

高校信息资源共享平台工作原理图如图4-1所示：

![](/md/blog.012.png)

图4-1 系统工作原理图
## 4.2 系统结构设计
系统架构图属于系统设计阶段，系统架构图只是这个阶段一个产物，系统的总体架构决定了整个系统的模式，是系统的基础。高校信息资源共享平台的整体结构设计如图4-2所示。

![](/md/blog.013.png)

图4-2 系统结构图
## 4.3数据库设计
数据库是计算机信息系统的基础。目前，电脑系统的关键与核心部分就是数据库。数据库开发的优劣对整个系统的质量和速度有着直接影响。
### 4.3.1 数据库设计原则
数据库的概念结构设计采用实体—联系（E-R）模型设计方法。E-R模型法的组成元素有：实体、属性、联系，E-R模型用E-R图表示，是提示用户工作环境中所涉及的事物，属性则是对实体特性的描述。在系统设计当中数据库起着决定性的因素。下面设计出这几个关键实体的实体—关系图。
### 4.3.2 数据库实体
数据模型中的实体（Entity），也称为实例，对应现实世界中可区别于其他对象的“事件”或“事物”。例如，公司中的每个员工，家里中的每个家具。

本系统的E-R图如下图所示：

1、学生信息管理实体图如图4-3所示：

![](/md/blog.014.png)

图4-3学生信息管理实体图

2、课程信息管理实体图如图4-4所示：

![](/md/blog.015.png)

`   `图4-4课程信息管理实体图

3、教师信息管理实体图如图4-5所示：

![](/md/blog.016.png)

图4-5教师信息管理实体图

#########

### 4.3.3 数据库表设计
数据库的表信息属于设计的一部分，下面介绍数据库中的各个表的详细信息。

表4-1 allusers表

|列名|数据类型|长度|约束|
| :-: | :-: | - | :-: |
|id|int|11|NOT NULL|
|username|varchar|50|` `default NULL|
|pwd|varchar|50|` `default NULL|
|cx|varchar|50|` `default NULL|


表4-2 jiaoshixinxi表

|列名|数据类型|长度|约束|
| :-: | :-: | - | :-: |
|id|int|11|NOT NULL|
|addtime|varchar|50|default NULL|
|jiaoshigonghao|varchar|50|default NULL|
|mima|varchar|50|default NULL|
|xingming|varchar|50|default NULL|
|zhicheng|varchar|50|default NULL|
|xingbie|varchar|50|default NULL|
|shouji|varchar|50|default NULL|
|youxiang|varchar|50|default NULL|
|shenfenzheng|varchar|50|default NULL|
|zhaopian|varchar|50|default NULL|

表4-3：jiaoxueziyuan表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|` `int|11|NOT NULL |
|addtime|varchar|50|default NULL|
|bianhao|varchar|50|default NULL|
|mingcheng|varchar|50|default NULL|
|tupian|varchar|50|default NULL|
|leixing|varchar|50|default NULL|
|neirongjieshao|varchar|50|default NULL|
|ziliao|varchar|50|default NULL|
|shangchuanshijian|varchar|50|default NULL|
|jiaoshigonghaojiaoshigonghao|varchar|50|default NULL|
|xingming|varchar|50|default NULL|


表4-4：kechengxinxi表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|` `int|11|NOT NULL |
|addtime|varchar|50|default NULL|
|kechengbianhao|varchar|50|default NULL|
|kechengmingcheng|varchar|50|default NULL|
|keshi|varchar|50|default NULL|
|kaishishijian|varchar|50|default NULL|
|kechengneirong|varchar|50|default NULL|
|kechengrenwu|varchar|50|default NULL|
|fengmian|varchar|50|default NULL|

表4-5：xinwenzixun表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|` `int|11|NOT NULL |
|addtime|varchar|50|default NULL|
|biaoti|varchar|50|default NULL|
|jianjie|varchar|50|default NULL|
|neirong|varchar|50|default NULL|
|fabushijian|varchar|50|default NULL|
|faburen|varchar|50|default NULL|
|fengmian|varchar|50|default NULL|


# 5统详细设计
## 5.1前台首页功能模块
高校信息资源共享平台，在系统首页可以查看首页、课程信息、教学资源、新闻资讯、我的、跳转到后台等内容，如图5-1所示。

![](/md/blog.017.png)

图5-1前台首页功能界面图



学生信息登录、学生信息注册，在注册页面可以填写账号、姓名、手机、邮箱、身份证等信息进行注册、登录，如图5-2所

示。

![](/md/blog.018.png)


![](/md/blog.019.png)

图5-2学生信息注册、学生信息登录界面图
#########
课程信息，在课程信息页面通过填写课程编号、课程名称、课时、开始时间、课程内容、课程任务、封面等信息进行提交，如图5-3所示。在教学资源页面通过填写编号、名称、图片、类型、内容介绍、资料、上传时间、教师工号、姓名等信息进行点我收藏操作，如图5-4所示。

![](/md/blog.020.png)

图5-3课程信息界面图
#########
![](/md/blog.021.png)

图5-4教学资源界面图

## 5.2管理员功能模块
管理员登录，通过填写用户名、密码进行登录，如图5-5所示。

![](/md/blog.022.png)

图5-5管理员登录界面图

管理员登录进入高校信息资源共享平台可以查看个人中心、学生信息管理、教师信息管理、课程信息管理、教学资源管理、新闻资讯管理、学院信息管理、系统管理等信息。

学生信息管理，在学生信息管理页面中可以通过填写账号、姓名、性别、手机、邮箱、身份证、照片等内容进行详情、修改、删除，如图5-6所示。还可以根据需要对教师信息管理进行详情，修改等详细操作，如图5-7所示。

![](/md/blog.023.png)

图5-6学生信息管理界面图

![](/md/blog.024.png)

图5-7教师信息管理界面图

课程信息管理，在课程信息管理页面中可以查看课程编号、课程名称、课时、开始时间、课程内容、课程任务、封面等信息，并可根据需要对已有课程信息管理进行修改或删除等操作，如图5-8所示。

![](/md/blog.025.png)

图5-8课程信息管理界面图

教学资源管理，在教学资源管理页面中可以查看编号、名称、图片、类型、内容介绍、资料、上传时间、教师工号、姓名等信息，并可根据需要对已有教学资源管理进行修改或删除等详细操作，如图5-9所示。

![](/md/blog.026.png)

图5-9教学资源管理界面图

新闻资讯管理，在新闻资讯管理页面中可以查看标题、简介、内容、发布时间、发布人、封面等内容，并且根据需要对已有新闻资讯管理进行详情，修改或删除等详细操作，如图5-10所示。

![](/md/blog.027.png)

图5-10新闻资讯管理界面图

学院信息管理，在学院信息管理页面中可以查看学院名称、所属地区、学院级别、学院性质、学院类型、招生电话、学院邮箱、学院网站、学院地址、邮政编码、学院简介、图片等内容，并且根据需要对已有学院信息管理进行详情，修改或删除等详细操作，如图5-11所示。

![](/md/blog.028.png)

图5-11学院信息管理界面图

轮播图；该页面为轮播图管理界面。管理员可以在此页面进行首页轮播图的管理，通过新建操作可在轮播图中加入新的图片，还可以对以上传的图片进行修改操作，以及图片的删除操作，如图5-12所示。

![](/md/blog.029.png)

图5-12轮播图管理界面图


## 5.3学生信息功能模块
学生信息登录进入高校信息资源共享平台可以查看个人中心、教学资源管理、新闻资讯管理等内容。

教学资源管理，在教学资源管理页面中通过填写编号、名称、图片、类型、内容介绍、资料、上传时间、教师工号、姓名等信息，还可以根据需要对教学资源管理进行修改，如图5-13所示。

![](/md/blog.030.png)

图5-13教学资源管理界面图

新闻资讯管理，在新闻资讯管理页面中可以查看标题、简介、内容、发布时间、发布人、封面等信息，并且根据需要对已有新闻资讯管理进行查看删除等其他详细操作，如图5-14所示。

![](/md/blog.031.png)

图5-14新闻资讯管理界面图
#########
## 5.4教师信息功能模块
教师信息登录进入高校信息资源共享平台可以查看个人中心、学生信息管理、课程信息管理、教学资源管理等内容。

学生信息管理，在学生信息管理页面中通过填写账号、姓名、性别、手机、邮箱、身份证、照片等信息，还可以根据需要对学生信息管理进行修改，如图5-15所示。

![](/md/blog.032.png)

图5-15学生信息管理界面图

课程信息管理，在课程信息管理页面中可以查看课程编号、课程名称、课时、开始时间、课程内容、课程任务、封面等信息，并且根据需要对已有课程信息管理进行查看删除等其他详细操作，如图5-16所示。

![](/md/blog.033.png)

图5-16课程信息管理界面图
#########
教学资源管理，在教学资源管理页面中通过填写编号、名称、图片、类型、内容介绍、资料、上传时间、教师工号、姓名等内容进行详情、修改、删除，如图5-17所示。

![](/md/blog.034.png)

图5-17教学资源管理界面图
#########












