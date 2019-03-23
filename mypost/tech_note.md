# 前台

## Web 发展历史

Web设计初衷是一个静态信息资源发布媒介，通过超文本标记语言（HTML）描述信息资源，通过统一资源标识符（URI）定位信息资源，通过超文本转移协议（HTTP）请求信息资源。

用通俗的一点的话来说，客户端（一般为浏览器）通过URL找到网站(如www.google.com)，发出HTTP请求，服务器收到请求后返回HTML页面。

阶段

- Web 诞生
- 动态内容出现：CGI
- Web 编程脚本语言：PHP / ASP / JSP
- 分布式企业计算平台：J2EE / .NET
- 框架横飞的年代：MVC，ORM
- 回归 Web 本质：REST
- 浏览器的魔术：Ajax
- 前端MVC：Angular / Backbone
- Javascript 在服务端的逆袭：NodeJs

时间线

1. 1991年8月6日，Tim Berners Lee在alt.hypertext新闻组贴出了一份关于World Wide Web的简单摘要，标志了Web页面在Internet上的首次登场。
2. Berners Lee在1993年建立了万维网联盟（World Wide Web Consortium，W3C），负责Web相关标准的制定。
3. 1993年CGI（Common Gateway Interface）出现了，Web上的动态信息服务开始蓬勃兴起。
4. 于是1994年的时候，PHP诞生了，PHP可以把程序（动态内容）嵌入到HTML（模版）中去执行，不仅能更好的组织Web应用的内容，而且执行效率比CGI还更高。
5. 1995年NetScape公司设计的JavaScript被用作浏览器上运行脚本语言为网页增加动态性。
6. 之后96年出现的ASP和98年出现的JSP本质上也都可以看成是一种支持某种脚本语言编程（分别是VB和Java）的模版引擎。
7. 96年W3C发布了CSS1.0规范。CSS允许开发者用外联的样式表来取代难以维护的内嵌样式，而不需要逐个去修改HTML元素，这让HTML页面更加容易创建和维护。
8. Web开始广泛用于构建大型应用时，在分布式、安全性、事务性等方面的要求催生了J2EE(现在已更名为Java EE)平台在1999年的诞生，
9. 2000年随之而来的.net平台，其ASP.net构件化的Web开发方式以及Visual Stidio.net开发环境的强大支持，大大降低了开发企业应用的复杂度。
10. 2001年出现的Hibernate就是其中的佼佼者，已经成为Java持久层的规范JPA的主要参考和实现。
11. 比如2003年出现的Java开发框架Spring
12. 2004年出现的Struts就是当时非常流行的Java Web开发的MVC框架。
13. 2005年出现的AJAX这个概念使得JavaScript再次大放异彩。
14. 2004年出现的Ruby开发框架Rails
15. 2005出现的Python开发框架Django

参考链接

- [Web开发技术发展历史](https://www.tianmaying.com/tutorial/web-history)
- [Web开发技术的演变](http://blog.jobbole.com/45170/)


## 切图

- 取色：可以用 FSCapture 来取
- 字号大小：PS里一般用 pt 单位，要转换成网页上的px
- 字体设置：  font-family: -apple-system, system-ui, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, "PingFang SC", "Hiragino Sans GB", "Microsoft YaHei", sans-serif;
- 测量间距
	- "编辑"-"首选项"-"单位与标尺", 把单位设置为像素 px
	- "视图"-"标尺"（Ctrl+R） 把标尺显示出来
	- 按住 Shift 键盘，从标尺拖出参考线，会自动对齐物体的边缘
	- 工具栏中选择标尺工具，按住 Shift 键（会自动垂直或水平），先点击第一条辅助线，再拖动到第二条辅助线，然后看信息栏里的 W 和 H，表示宽和高的信息
	- 量完尺寸后可以"视图"-"清除参考线"
- 矢量 Logo 导出：
	- 通过图层的隐藏显示，找到 Logo 对应的矢量智能对象，
	- 右键点击图层，转换为智能对象	
	- 按住 Ctrl 单击智能对象图层，再 Ctrl + C 复制选中的内容
	- Ctrl + N 新建文件，图像宽高会根据复制内容大小自动选定，背景内容选择 "透明" 
	- Ctrl + V 粘贴内容，"文件"-"存储为 Web 所用格式"，格式选择 PNG-24, 存储即可，如选 PNG-8 可能会有毛刺
- 图片导出：
	- 打开移动工具，选项里把"自动选择"的勾打上，
	- 点击要切割的图片，图层面板一般会自动选择图片所在的图层，即使定位不到具体图层，也能定位到图层组
	- 如果该图片是组合图形，或者有图层效果，或者有一个背景图一个遮罩，则按住 Ctrl 选中多个图层，右键合并图层
	- 按住 Ctrl 单击图层，Ctrl + C， Ctrl + N, Ctrl + V， Ctrl + Shif + Alt + S
	

字体大小的设置单位，常用的有2种：px、pt。这两个有什么区别呢？
先搞清基本概念：px就是表示pixel，像素，是屏幕上显示数据的最基本的点；
pt就是point，是印刷行业常用单位，等于1/72英寸。

合并拷贝，背景导出


参考链接：

- [PT与PX区别](https://www.douban.com/note/155032221/)
- [ps标尺和参考线知识点及快捷键](http://www.ittribalwo.com/article/1625.html)


## 经典页面

- [Alloy Timer](http://alloyteam.github.io/AlloyTimer/)
- http://www.raiseai.com/

## 常见任务
垂直居中

```
parentElement{
	position:relative;
}

childElement{
	position: absolute;
	top: 50%;
	transform: translateY(-50%);
}
```

### 左右等高

- [4 Methods For Creating Equal Height Columns In CSS](http://vanseodesign.com/css/equal-height-columns/)
- [Fluid Width Equal Height Columns](https://css-tricks.com/fluid-width-equal-height-columns/)
- [CSS布局——左定宽度右自适应宽度并且等高布局](https://www.w3cplus.com/css/two-cloumn-width-one-fixed-width-one-fluid-width)
- [Equal Height Column Layouts with Borders and Negative](https://www.smashingmagazine.com/2010/11/equal-height-columns-using-borders-and-negative-margins-with-css/)


### 背景图全屏

```
html,body{
    width:100%;
    height:100%
}

body{
	width: 100%;
  	height:auto;
	background:#343434 url("../../assets/img/bg.jpg") no-repeat;  
	background-size: cover;
}
```

## 参考链接

- [CSS Stacking Context里那些鲜为人知的坑](http://blog.angular.in/css-stacking-contextli-na-xie-xian-wei-ren-zhi-de-keng/)
- [HTML 和 Body 在 CSS 中的区别](https://csspod.com/html-vs-body-in-css/)
- [等宽列背后的表格布局算法](https://csspod.com/table-width-algorithms/)
- [Appendix D. Default style sheet for HTML 4](https://www.w3.org/TR/CSS2/sample.html)
- [学习CSS布局](https://www.w3cplus.com/css/learn-css-layout.html)
- [w3school HTML 系列教程](http://www.w3school.com.cn/h.asp)
- [CSS参考手册](http://www.css88.com/book/css/)
- [10 个最常见的 JavaScript 错误（以及如何避免它们）](http://www.css88.com/archives/9184)

## todo

- rem



# 后台


## 算法

[编程之法：面试和算法心得](https://github.com/julycoding/The-Art-Of-Programming-By-July)



InfraredCounterParser InfraredCounterHandler InfraredCounterSender 等字符串，取出最后一个单词，如Parser, Handler, Sender 等

中英文混排，如何在英文和数字两边增加空格

# 数据库
# 网络

# Java

- [Google Guava官方教程（中文版）](http://ifeve.com/google-guava/)
- [Windows7下Maven环境搭建及其使用](http://blog.csdn.net/xuexiaoxu1990/article/details/52882664)

## 环境变量配置



CLASSPATH= .;%JAVA_HOME%/lib/dt.jar;%JAVA_HOME%/lib/tools.jar

JAVA_HOME = C:/Program Files/Java/jdk1.5.0

PATH  = %JAVA_HOME%/bin;%JAVA_HOME%/jre/bin





参考

- [classpath、path、JAVA_HOME的作用及JAVA环境变量配置](https://www.cnblogs.com/xwdreamer/archive/2010/09/08/2297098.html)

# 软件工程
## 代码风格

[编程之法：面试和算法心得 Code Style](https://github.com/julycoding/The-Art-Of-Programming-By-July)

## UML

### 类图

- 泛化: 泛化(generalization)：表示is-a的关系，是对象之间耦合度最大的一种关系，子类继承父类的所有细节。直接使用语言中的继承表达。在类图中使用带三角箭头的实线表示，箭头从子类指向父类。
- 实现（Realization）:在类图中就是接口和实现的关系。在类图中使用带三角箭头的虚线表示，箭头从实现类指向接口。
- 依赖(Dependency)：对象之间最弱的一种关联方式，是临时性的关联。代码中一般指由局部变量、函数参数、返回值建立的对于其他对象的调用关系。一个类调用被依赖类中的某些方法而得以完成这个类的一些职责。在类图使用带箭头的虚线表示，箭头从使用类指向被依赖的类。
- 关联(Association) : 对象之间一种引用关系，比如客户类与订单类之间的关系。这种关系通常使用类的属性表达。关联又分为一般关联、聚合关联与组合关联。在类图使用带箭头的实线表示，箭头从使用类指向被关联的类。可以是单向和双向。
- 聚合(Aggregation) : 表示has-a的关系，是一种不稳定的包含关系。较强于一般关联,有整体与局部的关系,并且没有了整体,局部也可单独存在。如公司和员工的关系，公司包含员工，但如果公司倒闭，员工依然可以换公司。在类图使用空心的菱形表示，菱形从局部指向整体。
- 组合(Composition) : 表示contains-a的关系，是一种强烈的包含关系。组合类负责被组合类的生命周期。是一种更强的聚合关系。部分不能脱离整体存在。如公司和部门的关系，没有了公司，部门也不能存在了；调查问卷中问题和选项的关系；订单和订单选项的关系。在类图使用实心的菱形表示，菱形从局部指向整体。

参考

- [UML类图与类的关系详解](http://www.uml.org.cn/oobject/201104212.asp)

## 需求工程



### 需求分类

软件需求包括3个不同的层次――业务需求、用户需求和功能需求。除此之外，每个系统还有各种非功能需求。 

- **业务需求**（Business requirement）表示组织或客户高层次的目标。业务需求描述了组织为什么要开发一个系统，即组织希望达到的目标。
- **用户需求**（user requirement）描述的是用户的目标，或用户要求系统必须能完成的任务,用户能使用系统来做些什么。用例、场景描述和事件都是表达用户需求的有效途径。 
- **功能需求**（functional requirement）规定开发人员必须在产品中实现的软件功能，用户利用这些功能来完成任务，满足业务需求。如“系统应该发送电子邮件来通知用户已接受其预定”。
- **系统需求**（system requirement）用于描述包含多个子系统的产品（即系统）的顶级需求。系统可以只包含软件系统，也可以既包含软件又包含硬件子系统
- **非功能需求** 为满足用户业务需求而必须具有且除功能需求以外的特性
  - 安全性
  - 可靠性
  - 易用性
  - 可维护性
  - 可移植性

### 需求开发



需求开发活动包括以下几个方面：

1. 确定用户分类
2. 获取每类用户的需求
3. 了解实际用户任务和目标
4. 分析源于用户的信息以获取用户任务需求、功能需求、业务规则、质量属性、建议解决方法和附加信息
5. 将系统级的需求分为几个子系统
6. 了解相关质量属性的重要性
7. 商讨实施优先级的划分
8. 编写成规格说明和模型。
9. 评审需求规格说明


### 用例描述

用例图描述了参与者要求系统能“做什么”，但是缺乏描述系统该“怎么做”的细节。一般情况下，每个用例应具有一个用例描述。

#### 用例描述说明



- **用例名称**：用例名称应该表明用户的意图或用例的用途，例如：借阅图书、归还图书、预定图书等。
- **用例编号**： UC 0001
- **简要说明**：对用例进行简要说明，描述该用例的作用，说明应当简明扼要。
- **参与者**：与此用例相关的参与者列表
- **前置条件**：执行用例之前系统必须满足的条件，例如：当学生借阅图书时，借阅图书用例需要获取学生的借阅证信息，如果学生使用了一个已经被注销的借阅证，那么借阅图书用例就不能执行。
- **后置条件**：后置条件将在用例成功完成以后得到满足，它提供了系统的部分描述。例如：当学生借阅图书成功后，借阅图书用例应该提供该学生的所有借阅信息。
- **基本操作流程**：指参与者在用例中所遵循的主逻辑路径。例如，借阅图书用例的基本操作流程如下：
  - (1) 图书管理员输入借阅证信息
  - (2) 系统检查读者是否有超期的借阅信息
  - (3) 系统检查读者的借书数量是否已经达到借书限额
  - (4) 图书管理员输入要借阅的图书信息
  - (5) 系统将读者的借阅信息保存到数据库中
- **可选操作流程**：指参与者在用例中所遵循的次逻辑路径，通常是指出现异常或发生错误的情况下所遵循的路径。
- **涉及数据**：填写该用例涉及的相关信息，如图书名字，价格，ISBN号，出版日期等

#### 完整用例示例



| 主执行者      | 请求者                                      |
| --------- | ---------------------------------------- |
| 语境中的目标    | 请求者通过系统买东西，并得到说买的东西。不包括付款方面的内容。          |
| 范围        | 业务——整个购买机制，包括电子的和非电子的，正如人们在公司中说见到的一样。    |
| 层次        | 概要                                       |
| 项目相关人员和利益 | 请求者：希望得到她订购的东西，并且操作要简单。公司：希望控制花费，但允许必要的购买。供货商：希望得到任何已发货物的货款。 |
| 前置条件      | 无                                        |
| 最小保证      | 每一个发出的订单都已经获得有效认证者的许可。订单具有可跟踪性，以便公司只对收到的有效货物开账单。 |
| 成功保证      | 求者得到货物，修改预算，记入借方。                        |
| 触发事件      | 请求者决定买东西。                                |
| 主成功场景     | 1. 请求者：发起一个请求。2.   批准者：检查预算中的资金，检查货物的价格，完成提交请求。3. 买者：检查仓库的存货，找出最好的供货商。4. 认证者：验证批准者的签名。5. 买者：完成订购请求，向供货商发出PO（订单）。6. 供货商：把货物发送给接收者，得到发货收据（这一点超出了本系统的设计范围）。7. 接收者：记录发货情况；向请求者发送货物。8. 请求者：设置请求已被满足标志。 |
| 扩展        | 1a）请求者不知道供货商和货物价格：不填写这些内容，然后继续。1b）在收到货物之前的任意时刻，请求者都可以修改或取消请求：如果取消，则把这个请求从执行处理中取消。（从系统中删除吗？）如果降低价格，则不影响其处理过程。如果提高价格，则把请求送回批准者。2a）批准者不知道供货商或货物价格：不填写这些内容，留待买者填写或返回。2b）批准者不是请求者的经理：只是批准者签名仍然可行。2c）批准者拒绝申请：送回给请求者，要其修改或删除。3a）买者在仓库中找到货物：将存货先发出，并从申请者要求的总购买者中减去已经发出的这部分货物量，然后继续。3b）买者填写在前面活动中没有填写的供货商和价格信息：请求重新发回给批准者。4a）认证者拒绝批准者：发回请求者，并将此请求从执行处理中取消。5a）请求涉及到多个供货商：买者创建多个PO5b）买者将多个请求合并：相同的过程，但是用被合并的请求标记PO6a）供货商没有按时发货：系统发出没有发货警告。7a）部分发货：接收者在PO上做部分发货标记，然后继续。7b）多个请求PO的部分发货：接收者给每个请求分配货物数量，然后继续。8a）货物不对或质量不合格：请求者拒绝接收所发送的货物。8b）请求者已经离开公司：买者同请求者的经理进行核实，或者重新指派申请者，或者返还货物并取消请求。 |
| 技术和数据变动列表 | 无                                        |
| 优先级       | 多种                                       |
| 发行版本      | 几个                                       |
| 响应时间      | 多样                                       |
| 使用频率      | 3/天                                      |
| 主执行者的渠道   | 网络浏览器、邮件系统或类似系统                          |
| 次要执行者     | 供货商                                      |
| 次要执行者的渠道  | 传真、电话或汽车                                 |
| 未解决的问题    | 什么时候从系统中删除被取消的请求？要取消一个请求需要那些权限？谁能修改一个请求的内容？请求中需要保留哪些修改历史记录？当请求者拒绝已经发送的货物时，会发生什么情况？申请和订货在运作上有什么不同？ 订购如何参考和使用内部存货？ |

#### 用例执行步骤的10大准则

（1）使用简单的语法；
句子结构应该非常简单：主语……谓语动词……直接宾语……前置短语
例如                  系统……从帐户余额中扣除……一定数量……

（2）明确地写出“谁控制球”；
作者举了踢足球的场景的例子，说明了不管步骤的执行者如何变化，都要遵循（1）描述的格式。

（3）从俯视的角度来编写用例；
从用户的角度来写用例，而不是从系统内部来描述系统

~~（4）显示过程向前推移；~~

（5）显示执行者的意图而不是动作；
通过操纵系统的用户界面来描述用户的动作，这是在编写用例时常见的一种严重错误，它使得编写的目标处于一个很低的层次。我把它叫做“界面细节描述（interface detail description）”。在需求文档中，我们只关心界面所要达到的意图，总结在执行者之间传递的信息。可将这些低层次的步骤合并成一个步骤。

~~（6）包含“合理”的活动集；~~

（7）“确认”而不是“检查是否”
这是一个经常犯的错误，写用例不是写程序流程，不需要用选择语法，需要选择的时候，在扩展场景里体现

（8）可选择地提及时间限制；

（9）习惯用语：“用户让系统A与系统B交互”；
要分开来写，用户与系统A怎么怎么样，然后系统A和系统B怎么怎么样，这样用户才能看的懂。

（10）习惯用语：“循环执行步骤X到Y，直到条件满足”；
同（7），但如果需要重复的话，可直接在重复的步骤的前面和后面说明即可。

总之，这10大原则，目的就是为了让用例成为用户和开发人员沟通的桥梁，所以语言要简单易懂，而且要逻辑清晰。

### 参考链接



- [需求入门： 需求工程＝需求开发＋需求管理](http://www.uml.org.cn/RequirementProject/201005285.asp)
- [软件需求规格说明书模板](https://jingyan.baidu.com/article/6dad5075eae10da123e36e80.html)
- [描述用例](http://blog.csdn.net/wlanye/article/details/7445676)
- [软件需求3个层次――业务需求、用户需求和功能需求](https://www.cnblogs.com/litian/articles/2047981.html)
- [非功能性六大点](https://jingyan.baidu.com/article/90bc8fc80960f1f653640ce0.html)
- [《编写有效用例》学习笔记](http://lib.csdn.net/article/softwaretest/24322)





## 文档

### 文档列表

1. 可行性分析报告
2. 项目开发计划
3. **软件需求说明书**
4. **概要设计说明书**
5. 详细设计说明书
6. **用户操作手册、运维部署文档**
7. 测试计划
8. 测试分析报告
9. 开发进度月报
10. 项目开发总结报告
11. 软件维护手册
12. 软件问题报告
13. 软件修改报告 

### 需求分析文档

内容

- 项目背景
- 使用角色
- 功能需求
  - 功能划分
  - 用例图
  - 用例描述
- 性能需求
  - 用户数评估
  - 响应时间要求
  - 可靠性需求
- 用户界面

### 概要设计文档

对大部分的公司来说，概要设计文档是唯一的设计文档，对后面的开发、测试、实施、维护工作起到关键性的影响。

内容

- 功能介绍
  - 用例图
- 整体架构
  - 层次结构
  - 模块划分
  - 模块间调用关系
  - 包图、组件图
- 接口设计
  - 对外接口草案
  - 模块间接口草案
- 模块设计
  - 职责描述
  - 类图
  - 算法描述（如有）
- 数据流设计
  - 流程图
  - 序列图
  - 状态图
- 数据库概要设计
  - 表设计
  - 核心语句
- 主要界面
- 部署结构
  - 部署图
- 非功能需求
  - 性能需求
  - 安全需求
  - 扩展性需求
- 编码规范
  - 代码风格
  - 数据库命名规范
  - 接口规范

### 详细设计文档

同概要设计文档，只是需要更详细，比如

- 类图要精确到字段，方法的类型，
- 数据库设计要精确到字段类型，索引设计
- 核心算法要画出序列图及伪代码

### 运维部署文档

内容

- 硬件需求
- 软件需求
- 外部依赖
- 部署步骤
- 配置说明
- 维护命令：启动、停止、重启
- 监控指标
- 如何升级
- 常见问题处理
- 数据备份

### 参考链接

- [软件开发文档范例](http://zz563143188.iteye.com/blog/1835305)
- [概要设计文档编写规范](http://blog.csdn.net/nengyu/article/details/3758312)

# 工具

## 其它

- [f.lux - 全天候保护眼睛健康软件！自动调整屏幕色温减少蓝光防疲劳，长时间玩电脑必备！](https://www.iplaysoft.com/flux.html)
- [MarkDown 写 ppt](https://yhatt.github.io/marp/)
- [在线根据 markdown 生成 ppt](http://www.vmfor.com/ppt/index.html)

## 编辑器



### 功能需求



- 行号显示
- 语法高亮
- 自动识别编码
- 自动缩进
- 智能提示
- 列编辑
- 代码片段
- 代码折叠
- 新建文件模板
- 多标签
- 会话管理
- 分屏
- 书签
- 多次光标点跳转

### VS Code

快捷键

- 注释切换：ctrl +／
- 格式化代码： Alt + Shift + F
- 自动换行：Alt + Z
- 选区移动：Alt + ↑/↓
- 多选修改：Ctrl + D

### Eclipse

- 格式化代码：Ctrl + Shift + F

参考链接：

- [为什么我选择使用 VS Code进行前端开发?](https://zhuanlan.zhihu.com/p/28631442)
- [TextMate代码片段语法](https://manual.macromates.com/en/snippets)

# 物联网

## 参考链接

[关于RS232 和 RS485 的区别](http://blog.csdn.net/foreverhuylee/article/details/23375079)

## 硬件技术


### 串口

串行接口（Serial port）又称“串口”，主要用于串行式逐位数据传输。

串行接口按电气标准及协议来分，包括RS-232-C、RS-422、RS485、USB等。

- RS-232-C、RS-422与RS-485标准只对接口的电气特性做出规定，不涉及接插件、电缆或协议。
- USB是近几年发展起来的新型接口标准，主要应用于高速数据传输领域。

**RS-232-C ：也称标准串口**，是目前最常用的一种串行通讯接口。电脑一般有两个串行口：COM1和COM2，9针D形接口通常在计算机后面能看到。

**RS-485** ：为扩展应用范围，增加了多点、双向通信能力，即允许多个发送器连接到同一条总线上，同时增加了发送器的驱动能力和冲突保护特性，扩展了总线共模范围。

**Universal Serial Bus（通用串行总线） ：简称USB，** USB接口是电脑主板上的一种四针接口，其中中间两个针传输数据，两边两个针给外设供电。USB接口速度快、连接简单、不需要外接电源，传输速度12Mbps，新的USB 2.0可达480Mbps；

**RJ-45接口** ：是以太网最为常用的接口， 8个位置（8针）的模块化插孔或者插头



串口属性：

-  PortName 串口名
-  BaudRate 获取或设置串行波特率bit/s    默认值9600
-  DataBits 获取或设置每个字节的标准数据位长度    默认值8
-  StopBits 获取或设置每个字节的标准停止位数    默认值One
-  Parity 获取或设置奇偶校验检查协议    默认值None



参考

- [C#中的串口通信](http://www.cnblogs.com/51net/p/6050840.html)

### IC卡，ID卡，M1卡，射频卡的区别

IC卡全称集成电路卡（Integrated Circuit Card），又称智能卡（Smart Card）。可读写，容量大，有加密功能，数据记录可靠，使用更方便，如一卡通系统、消费系统等

ID卡全称身份识别卡（Identification Card），是一种不可写入的感应卡，含固定的编号，

[门禁卡是选择IC卡好还是ID卡好](https://jingyan.baidu.com/article/54b6b9c0d8056f2d593b474c.html)




### RFID

从概念上来讲，RFID类似于[条码扫描](https://baike.baidu.com/item/%E6%9D%A1%E7%A0%81%E6%89%AB%E6%8F%8F)，对于条码技术而言，它是将已编码的条形码附着于目标物并使用专用的扫描读写器利用光信号将信息由条形磁传送到扫描读写器；而RFID则使用专用的RFID读写器及专门的可附着于目标物的RFID标签，利用频率信号将信息由RFID标签传送至RFID读写器。

[射频识别系统](https://baike.baidu.com/item/%E5%B0%84%E9%A2%91%E8%AF%86%E5%88%AB%E7%B3%BB%E7%BB%9F)最重要的优点是非接触识别，它能穿透雪、雾、冰、[涂料](https://baike.baidu.com/item/%E6%B6%82%E6%96%99)、[尘垢](https://baike.baidu.com/item/%E5%B0%98%E5%9E%A2)和条形码无法使用的恶劣环境阅读标签，并且阅读速度极快，大多数情况下不到100毫秒。

一维条形码的容量是50Bytes，二维条形码最大的容量可储存2至3000字符，RFID最大的容量则有数MegaBytes.

现今的条形码印刷上去之后就无法更改，RFID标签则可以重复地新增、修改、删除RFID卷标内储存的数据，方便信息的更新。

### NFC

NFC近场通信技术是由非接触式[射频识别](https://baike.baidu.com/item/%E5%B0%84%E9%A2%91%E8%AF%86%E5%88%AB)（[RFID](https://baike.baidu.com/item/RFID)）及互联互通技术整合演变而来，在单一芯片上结合感应式[读卡器](https://baike.baidu.com/item/%E8%AF%BB%E5%8D%A1%E5%99%A8)、感应式卡片和点对点的功能，能在短距离内与兼容设备进行识别和[数据交换](https://baike.baidu.com/item/%E6%95%B0%E6%8D%AE%E4%BA%A4%E6%8D%A2)。

NFC手机内置NFC芯片，比原先仅作为标签使用的RFID更增加了数据双向传送的功能，这个进步使得其更加适合用于电子货币支付的；

NFC传输范围比RFID小，RFID的传输范围可以达到几米、甚至几十米，但由于NFC采取了独特的信号衰减技术，相对于RFID来说NFC具有距离近、带宽高、能耗低等特点。

应用方向不同。NFC看更多的是针对于消费类电子设备相互通讯，有源RFID则更擅长在长距离识别。

NFC的短距离通信特性正是其优点，由于耗电量低、一次只和一台机器链接，拥有较高的保密性与安全性，NFC有利于信用卡交易时避免被盗用。

### PLC

### 继电器

继电器是具有隔离功能的自动开关元件，广泛应用于遥控、遥测、通讯、自动控制、机电一体化及电力电子设备中，是最重要的控制元件之一。

继电器一般都有能反映一定输入变量（如电流、电压、功率、阻抗、频率、温度、压力、速度、光等）的感应机构（输入部分）；有能对被控电路实现“通”、“断”控制的执行机构（输出部分）；在继电器的输入部分和输出部分之间，还有对输入量进行耦合隔离，功能处理和对输出部分进行驱动的中间机构（驱动部分）。

### 二进制协议

二进制常用操作

```

	int value = 170;
	void print(int x) => Console.WriteLine(Convert.ToString(x, 2).PadLeft(8, '0'));
	int make_mask(int x) => 1 << x;
	int set(int x, int i) => x | make_mask(i);
	int unset(int x, int i) => x & ~make_mask(i);
	bool isset(int x, int i) => (x & make_mask(i)) != 0;

	//170的二进制显示：                    10101010
	print(value);

	// 右数第 5 位置 1 ：                  10111010
	print(set(value, 4));

	// 右数第 4 位置 0：                   10100010
	print(unset(value, 3));

	// 右数第 4 位是否为1:                 true
	Console.WriteLine(isset(value, 3));

	//右数第 3 位是否为1:                  false
	Console.WriteLine(isset(value, 2));
```

### 其它

TTL电平信号之所以被广泛使用，原因是：通常我们采用二进制来表示数据。而且规定，+5V等价于逻辑“1”，0V等价于逻辑“0”。这样的数据通信及电平规定方式，被称做TTL（晶体管-晶体管逻辑电平）信号系统。这是计算机处理器控制的设备内部各部分之间通信的标准技术。

GND是电线接地端的简写。代表地线或0线。这个地并不是真正意义上的地，是出于应用而假设的一个地，对于电源来说，它就是一个电源的负极。

VCC：电源电压(双极器件);电源电压(74系列数字电路);

RXD 为接收数据的引脚，TXD 为发送数据的引脚。

DTE提供或接收数据，连接到调制解调器上的计算机就是一种DTE。DTE提供或接收数据，连接到网络中的用户端机器，主要是计算机和终端设备。

在网络端的连接设备称为DCE（Data-Communication Equipment）。DTE与进行信令处理的DCE相连。
DTE通过DCE设备，例如，调制解调器，连接到数据网络。

RS232标准中的RTS与CTS：即请求发送/清除发送，用于半双工时的收发切换，属于辅助流控信号。半双工的意思是说，发的时候不收，收的时候不发。那么怎么区分收发呢？缺省时是DCE向DTE发送数据，当DTE决定向DCE发数据时，先有效RTS，表示DTE希望向DCE发送。一般DCE不能马上转换收发状态，DTE就通过监测CTS是否有效来判断可否发送，这样避免了DTE在DCE未准备好时发送所导致的数据丢失。

差分输入的是将两个输入端的差值作为信号，这样可以免去一些误差，比如你输入一个1V的信号电源有偏差，比实际输入要大0.1.就可以用差分输入1V和2V一减就把两端共有的那0.1误差剪掉了。单端输入无法去除这类误差。

在某些系统里，系统'地'被用作电压基准点。当'地'当作电压测量基准时，这种信号规划被称之为单端的。

差分信号的第一个好处是，因为你在控制'基准'电压，所以能够很容易地识别小信号。
差分信号的第二个主要好处是，它对外部电磁干扰（EMI）是高度免疫的。
差分信号提供的第三个好处是，在一个单电源系统，能够从容精确地处理'双极'信号。

上拉就是将不确定的信号通过一个电阻钳位在高电平，电阻同时起限流作用。下拉同理，也是将不确定的信号通过一个电阻钳位在低电平。

# 企业信息化

大多数OA产品功能集中在信息共享、行政办公领域，一些主流OA系统虽然引入了工作流，但相对比较封闭，开放性和扩展性不够。

BPM是一个开放性平台，不仅能实现所有OA的功能，还能满足企业内部系统之间集成的需求，在BPM引擎驱动下，企业的流程终会形成一个闭环。

ERP

WMS

MES

ESB

SOA

- [智能MES解决方案](http://www.rtdsoft.com/channels/57.html)
- [制造执行系统(MES)选型与实施指南简版](https://wenku.baidu.com/view/052b5ef4a32d7375a41780c8.html)
- [OpenMES架构说明书](https://wenku.baidu.com/view/2a98711ec281e53a5802ffc8.html)

## 快速开发框架

- 登录注册: Apache Shiro 
- 组织机构
- 权限管理: Apache Shiro 
- 增删改查
- 后台界面
- 菜单管理
- 工作流：Activity
- 报表：JasperReports

参考

- http://www.jeecg.org/
- [Java通用权限系统管理（Spring+springMVC+ibatis+Angularjs）](http://46aae4d1e2371e4aa769798941cef698.devproxy.yunshipei.com/liaodehong/article/details/53100313)
- [组织机构对象模型设计及实现](http://blog.csdn.net/wangpeng047/article/details/7280800)
- [LigerUI 快速开发UI框架](http://www.ligerui.com/)
- https://github.com/thinkgem/jeesite

jeesite应用实战（数据增删改查），认真读完后10分钟就能开发一个模块
http://blog.csdn.net/qing_gee/article/details/76223064


# 未整理

[Avoid calling Invoke when the control is disposed](https://stackoverflow.com/questions/1874728/avoid-calling-invoke-when-the-control-is-disposed)



http://blog.csdn.net/pkueecser/article/details/50610796 时间序列数据库的秘密



https://github.com/justjavac/ReplaceGoogleCDN Replace Google CDN

https://stackoverflow.com/questions/31572580/how-covert-c-sharp-datetime-to-java-datetimeusing-joda-time
https://pine.fm/LearnToProgram/
http://www.qdaily.com/articles/42060.html
https://zh.wikihow.com/%E5%AD%A6%E4%B9%A0%E7%BC%96%E7%A8%8B

nginx waf

前端系列教程
https://chuanke.baidu.com/s5508922.html
http://growth.phodal.com/

关于PHP程序员解决问题的能力
http://www.cnblogs.com/phpworld/p/8038581.html
ZH奶酪：编程语言入门经典100例【Python版】
http://www.cnblogs.com/CheeseZH/archive/2012/11/05/2755107.html
https://www.coursera.org/learn/python

JavaScript专题之惰性函数 https://segmentfault.com/a/1190000010783034
关于尾递归的问题 https://segmentfault.com/q/1010000002705723

var pi = 3.14;
function area(r) { return 2 * pi * r;}
function iseven(n) {return n % 2 == 0;}

function range(n, m) { console.log(n); (n < m) ? range(n + 1, m) : null;}
function rangef(n, m, f) { f(n);  (n < m) ? rangef(n + 1, m, f) : null;}
function rangesum(n, m, sum) { return n < m ? n + rangesum(n + 1, m, sum) : n + sum; }
function rangesumf(n, m, sum, f) { return n < m ? f(n) + rangesumf(n + 1, m, sum, f) : f(n) + sum; }
function rangecond(n, m, cond) { cond(n) ? console.log(n) : null; (n < m) ? rangecond(n + 1, m, cond) : null;}

7 of the Best Code Playgrounds
https://www.sitepoint.com/7-code-playgrounds/

Beginning Programming For Dummies
https://www.amazon.com/Beginning-Programming-Dummies-Wallace-Wang/dp/0470088702
jQuery File Upload跨域上传
https://www.cnblogs.com/ZHF/p/5057416.html
Javascript知识点：IIFE - 立即调用函数
https://linghucong.js.org/2016/04/25/2016-04-08-Javascript-IIFE/
技术面试需要掌握的基础知识
https://github.com/CyC2018/Interview-Notebook

### 函数组合
function rangei(n) {
	var i = 0;
	return function() {
		var ret = i < n ? i : null;
		i = i + 1;
		return ret;
	};
}

function mapi(i, f) {
	return function () {
		var t = i();
		return t == null ? null : f(t);
	};
}

function filteri(i, c) {
	return function inner() {
		var t = i();
		return t == null ? null : c(t) ? t : inner(); 
	};
}

function reducei(i, f, init_val) {
	var t = i();
	return t == null ? init_val : reducei(i, f, f(init_val, t));
}
	
function iseven(x) {
	return x % 2 == 0; 
}

function sqr(x) {
	return x * x;
}

function add(x, y) {
	return x + y;
} 

//10 以内偶数的平方和
reducei(mapi(filteri(rangei(10), iseven), sqr), add, 0)

Jquery mobile change page
https://stackoverflow.com/questions/9738948/jquery-mobile-change-page
The Truth About Multiple H1 Tags in the HTML5 Era
https://webdesign.tutsplus.com/articles/the-truth-about-multiple-h1-tags-in-the-html5-era--webdesign-16824

How to set up Spark on Windows?
https://stackoverflow.com/questions/25481325/how-to-set-up-spark-on-windows


Git for windows 中文乱码解决方案
https://segmentfault.com/a/1190000000578037
Best way to find if an item is in a JavaScript array? [duplicate]
https://stackoverflow.com/questions/143847/best-way-to-find-if-an-item-is-in-a-javascript-array
后台管理UI的选择
https://www.cnblogs.com/webenh/p/5815732.html

配置 PHP 错误日志

mkdir /data/logs/php
chown apache:apache /data/logs/php

php-fpm.conf：

    [global]
    ; php-fpm pid文件
    pid = /usr/local/php/var/run/php-fpm.pid
    ; php-fpm 错误日志路径
    error_log = /data/logs/php/error.log
    ; php-fpm 记录错误日志等级
    log_level = notice
    [www]
    ; 记录错误到php-fpm的日志中
    ;catch_workers_output = yes
    ; 慢日志
    slowlog = /data/logs/php/www-slow.log
    ; 关闭打印日志
    php_flag[display_errors] = off
    ; 错误日志
    php_admin_value[error_log] = /data/logs/php/www-error.log
    ; 记录错误
    php_admin_flag[log_errors] = on
    ; 内存使用量
    php_admin_value[memory_limit] = 32M

php.ini：

    ; 错误日志
    log_errors = On
    ; 显示错误
    display_errors = Off
    ; 日志路径
    error_log = "/usr/local/lnmp/php/var/log/error_log"
    ; 错误等级
    error_reporting = E_ALL&~E_NOTICE
    
    
nginx 路径匹配测试

    location /test {
        add_header Content-Type text/html;
        return 200 'hello';
    }

nginx php 测试

    chmod o+x /root
    chmod o+x /root/haohu
    chmod o+x /root/haohu/phptest
    
    location ~ /test$ {
        fastcgi_pass   127.0.0.1:9000;
        include        fastcgi_params;
        fastcgi_param SCRIPT_FILENAME /root/haohu/phptest/test.php;
    }
    
nginx 日志格式

    log_format  main  '$time_iso8601 $status $request_time $upstream_response_time $remote_addr '
                      '"$request" $body_bytes_sent "$http_referer" '
                      '"$http_user_agent" "$http_x_forwarded_for"';
                      
日志滚动

    /var/log/nginx/*.log
    /data/log/nginx/*.log
    /data/logs/techaction/*.php
    /data/logs/php/*.log
    /var/log/php-fpm/*log
    {
        daily
        rotate 30
        missingok
        notifempty
        compress
        sharedscripts

        postrotate
            /bin/kill -USR1 `cat /run/nginx.pid 2>/dev/null` 2>/dev/null || true
                /bin/kill -SIGUSR1 `cat /var/run/php-fpm/php-fpm.pid 2>/dev/null` 2>/dev/null || true
        endscript
    }
                      
    
Linux日志文件总管——logrotate
https://linux.cn/article-4126-1.html
Linux中find常见用法示例
http://www.cnblogs.com/wanqieddy/archive/2011/06/09/2076785.html

找到 /data/logs 目录下所有 15 天之前修改过的 .php 和 .log 文件删除掉，删除前加确认，去掉确认的话，把 -ok 改成 -exec
find /data/logs/ -type f \( -name '*.php' -o -name '*.log' \)  -mtime +15 -print -ok rm  {} \;    



防止文件误删：http://www.cnblogs.com/lihaozy/archive/2012/08/17/2643784.html

    mkdir -p ~/.trash
    alias rm=trash  
    alias r=trash  
    alias rl='ls ~/.trash'
    alias ur=undelfile

    undelfile()
    {
      mv -i ~/.trash/$@ ./
    }

    trash()
    {
      mv $@ ~/.trash/
    }
    
    cleartrash()
    {
        read -p "clear sure?[n]" confirm
        [ $confirm == 'y' ] || [ $confirm == 'Y' ]  && /usr/bin/rm -rf ~/.trash/*
    }
    
[译] Node.js 8: util.promisify()
https://segmentfault.com/a/1190000009743481
Node.js Async Best Practices & Avoiding the Callback Hell
https://blog.risingstack.com/node-js-async-best-practices-avoiding-callback-hell-node-js-at-scale/
Nodejs 中使用 Async/Await
https://www.jianshu.com/p/0837dde8dcd5

promisify + async 

    (async () => {
      const fs = require('fs');
      const util = require('util');

      const readFile = util.promisify(fs.readFile);

      const txt = await readFile('./notes.txt');
      console.log(txt);
    })();
    
好吧，CSS3 3D transform变换，不过如此！    
http://www.zhangxinxu.com/wordpress/2012/09/css3-3d-transform-perspective-animate-transition/    
客栈说书：CSS遮罩CSS3 mask/masks详细介绍
http://www.zhangxinxu.com/wordpress/2017/11/css-css3-mask-masks/
新手应该如何学习 PHP 语言？
https://www.zhihu.com/question/20003635/answer/338733500
目前最详细的PHP培训课程安排
http://baijiahao.baidu.com/s?id=1563138980186749&wfr=spider&for=pc

CSS3 box-pack 属性
http://www.w3school.com.cn/cssref/pr_box-pack.asp
设计一个灵活的、可维护CSS和SVG饼图SVG
https://www.jianshu.com/p/f6526355de54
SVG中stroke-dasharray及stroke-dashoffset属性
https://blog.csdn.net/u014291497/article/details/78409350   
纯CSS实现帅气的SVG路径描边动画效果
http://www.zhangxinxu.com/wordpress/2014/04/animateion-line-drawing-svg-path-%E5%8A%A8%E7%94%BB-%E8%B7%AF%E5%BE%84/

https://secbone.com/
https://github.com/Secbone

# 快速学习一门语言
- 打字练习：
    - 数字，字母，下划线
    - 标点符号：+-*/\%(){};"',.!<>[]?^|
- 输出
    - 打印字符串
    - 打印数字
    - 混合打印
    - 输出复杂信息
    - 格式化输出    
- 字符串连接
- 数学运算: + - * / %
- 关系运算: > < == != >= <=
- 逻辑运算: && || !
- 变量和赋值: =
- 条件语句和关系操作符：两个数谁最大
- 多重条件语句和逻辑操作符：三个数谁最大
- 循环语句：打印 5 次 Hello
- for 循环：打印 10 以内的偶数
- 数组基本操作
    - 打印数组
    - 获取数组长度
    - 获取指定索引元素
    - 修改指定索引元素的值
    - 数组末尾增加元素
    - 某元素是否存在
    - 遍历数组
    - 删除指定索引元素
    - 重排数组
    - 任意位置插入元素
    - 连接成字符串
    - 练习
        - 找出一个数组中最大的数
        - 找出一个数组中最大的奇数
        - 求出数组中所有奇数的和
- 字符串基本操作
    - 字符串长度
    - 字符串连接
    - 转换大小写
    - 去掉首尾指定字符
    - 用某字符在首尾填充    
    - 分割成数组
    - 比较两个字符串
    - 获取某子串的位置
    - 是否存在某个子串
    - 替换某个子串
    - 获取子串
    - 是否以某子串开头或结尾
    - 练习
        - 判断某字符是否为大写
        - 把字符串中的每个单词首字母大写
        - 按大写字母分割字符串
- 字典基本操作
    - 根据键获取值
    - 添加键值对
    - 修改键值对
    - 删除指定键
    - 某键是否存在
    - 遍历字典
- 时间操作
    - 设置时区
    - 获取当前时间的时间戳
    - 获取当前时间格式化字符串
- 文件操作：打开并逐行读取文件
- 类型判断
    - 是否为数字
    - 是否为整型
    - 是否为浮点数
    - 是否为字符串
    - 是否为 null
    - 是否为 数组
    - 是否为空
- 类型转换
    - 数字转字符串
    - 字符串转数字
- 函数
    - 函数定义和使用
    - 匿名函数和闭包
    - 返回函数的函数
    - 参数为函数的函数
    - 函数的递归调用
- 面向对象
    - 类
    - 方法
    - 字段
    - 静态字段
    - 子类

数组:
- get set remove insert length 
- push pop shift unshit slice indexof
- startswitch endswitch contains
- map filter reduce
- removeCond groupby sortby countby

字典
- add set get remove
树

输入输出文件

Android Studio:

- 下载带 Sdk 版本
- 修改字体
- 修改编码
- 自动提示快捷键修改
- 去掉拼写检查
- 设置 git 目录
- 禁用不需要的插件
- 自动导入
- File –> Other Settings –> Default Project Structure
- idea.properties  disable.android.first.run=true
- ANDROID_SDK_HOME 环境变量指向 D:\android-home 把 .android 目录拷过去
- 禁止自动打开上次的工程
- 禁止代码折叠

Android:

- 加载中效果
- 短暂提示
- 网络访问要用AsyncTask
- 小图标
- 全局错误挂接
- 优雅退出
- 打日志
- 每页的标题
- 返回按钮
- 导航条一直存在


安卓异步任务类AsyncTask——突出一个简单、好用
https://blog.csdn.net/jerrycqu/article/details/49357191
Android OkHttp的基本用法
https://www.jianshu.com/p/c478d7a20d03
Toolbar的简单使用
https://blog.csdn.net/monalisatearr/article/details/78415585
ListView中自定义adapter的封装
https://www.cnblogs.com/smyhvae/p/4477079.html
Gson解析——从简单数据到复杂数据
https://www.jianshu.com/p/886f7b7fca7d
LoadingBar - 如何更优雅的使用Loading
https://blog.csdn.net/aa464971/article/details/70197394
NavigationView的使用
https://blog.csdn.net/bskfnvjtlyzmv867/article/details/70245826
Android中处理崩溃异常
https://blog.csdn.net/liuhe688/article/details/6584143




Android Studio 入门级教程（
https://www.cnblogs.com/abao0/archive/2017/06/02/6934023.html

详解 Android 的 Activity 组件
https://www.ibm.com/developerworks/cn/opensource/os-cn-android-actvt/
Android之自定义Adapter的ListView
http://www.cnblogs.com/topcoderliu/archive/2011/05/07/2039862.html
想写个app，在哪里可以找到icon素材？
https://www.zhihu.com/question/40639915?sort=created
https://github.com/konifar/android-material-design-icon-generator-plugin
Android学习 - 美化ListView
https://blog.csdn.net/wolflz/article/details/45078107
Android开发之漂亮Button样式
https://www.jianshu.com/p/e5e8a98fc5d9


图标制作
https://www.iconfinder.com/editor/
https://www.flaticon.com/free-icons/programming-language/2
https://glyphter.com/
https://www.shutterstock.com/zh/image-vector/workplace-programmer-coder-desktop-pc-laptop-705161689?src=Kd61QRsGtq1hI9vEL7LU2w-1-49
https://iconsflow.com/editor

APP第三方微信登录与公众号数据打通
https://www.jianshu.com/p/18b1288f4c41

Flex 布局教程：语法篇
http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html
Flex 布局教程：实例篇
http://www.ruanyifeng.com/blog/2015/07/flex-examples.html

Programmed Lessons in QBasic
http://chortle.ccsu.edu/QBasic/index.html
中等职业教育国家规划教材·编程语言基础：QBASIC语言（计算机及应用专业）
https://item.jd.com/10493424.html

wget https://npm.taobao.org/mirrors/node/v8.9.3/node-v8.9.3-linux-x64.tar.xz

tar -xzvf node-v8.9.3-linux-x64.tar.gz
tar -xvf node-v8.9.3-linux-x64.tar
ln -s /root/node-v8.9.3-linux-x64/bin/node /usr/local/bin/node
ln -s /root/node-v8.9.3-linux-x64/bin/npm /usr/local/bin/npm
npm -v
npm install -g cnpm --registry=https://registry.npm.taobao.org

$ sudo npm install forever -g   #安装
$ forever start app.js          #启动
$ forever stop app.js           #关闭
$ forever start -l forever.log -o out.log -e err.log app.js   #输出日志和错误


## Apache backend for www.quancha.cn ##
upstream apachephp  {
    server ip:8080; #Apache
}
 
## Start www.quancha.cn ##
server {
    listen 80;
    server_name  www.quancha.cn;
 
    access_log  logs/quancha.access.log  main;
    error_log  logs/quancha.error.log;
    root   html;
    index  index.html index.htm index.php;
 
    ## send request back to apache ##
    location / {
        proxy_pass  http://apachephp;
 
        #Proxy Settings
        proxy_redirect     off;
        proxy_set_header   Host             $host;
        proxy_set_header   X-Real-IP        $remote_addr;
        proxy_set_header   X-Forwarded-For  $proxy_add_x_forwarded_for;
        proxy_next_upstream error timeout invalid_header http_500 http_502 http_503 http_504;
        proxy_max_temp_file_size 0;
        proxy_connect_timeout      90;
        proxy_send_timeout         90;
        proxy_read_timeout         90;
        proxy_buffer_size          4k;
        proxy_buffers              4 32k;
        proxy_busy_buffers_size    64k;
        proxy_temp_file_write_size 64k;
   }
}

How to easily convert utf8 tables to utf8mb4 in MySQL 5.5
https://dba.stackexchange.com/questions/8239/how-to-easily-convert-utf8-tables-to-utf8mb4-in-mysql-5-5

不翻墙也能找到免费优质素材，7个免费商用素材库墙裂推荐
https://zhuanlan.zhihu.com/p/28508804

微服务分布式事务Saga模式简介
http://www.jdon.com/49307

大数据告诉你：为啥近5年来Python如此火爆？
https://www.sohu.com/a/196290953_704222
kvm管理平台webvirtmgr的部署
https://www.jianshu.com/p/160272d81ac3
Comfortable interface for KVM? (with PCIe Passthrough)
https://www.centos.org/forums/viewtopic.php?t=52640

CentOS之7与6的区别
https://www.cnblogs.com/Csir/p/6746667.html
开源虚拟化管理平台Ovirt简介和配置环境搭建
https://www.2cto.com/os/201202/120678.html
libvirt apps
https://libvirt.org/apps.html#web
十分钟带你理解Kubernetes核心概念
http://dockone.io/article/932
使用 Docker/LXC 迅速启动一个桌面系统
https://www.oschina.net/question/54100_137626
在Docker中运行桌面应用
https://yq.aliyun.com/articles/224645#
docker-desktop
https://github.com/rogaha/docker-desktop
图形化界面的 docker ?
https://www.zhihu.com/question/34493859
Windows Docker 安装
http://www.runoob.com/docker/windows-docker-install.html
https://blog.csdn.net/tina_ttl/article/details/51372604
后端架构师技术图谱
https://github.com/xingshaocheng/architect-awesome/blob/master/README.md#%E6%95%B0%E6%8D%AE%E7%BB%93%E6%9E%84

termtosvg
A Linux terminal recorder written in Python that renders your command line sessions as standalone SVG animations.
https://github.com/nbedos/termtosvg

如何编写技术解决方案
https://wenku.baidu.com/view/b42e31a1760bf78a6529647d27284b73f2423635.html?from=search

p5.js 
http://ofcourse.io/biao-ti-3/

腾讯云 使用DockerHub加速器
https://cloud.tencent.com/document/product/457/9113
理解Docker（7）：Docker 存储 - AUFS
https://www.cnblogs.com/sammyliu/p/5931383.html
［授权发表］基于 ssh + Xpra 构建 Docker 桌面系统
https://blog.csdn.net/tinylab/article/details/45443563
CentOS6下docker的安装和使用
https://www.cnblogs.com/zhangzhen894095789/p/6641981.html?utm_source=itdadao&utm_medium=referral

How to stop docker pull
https://stackoverflow.com/questions/29486032/how-to-stop-docker-pull
DOCKER_OPTS do not work in config file /etc/default/docker
https://stackoverflow.com/questions/27763340/docker-opts-do-not-work-in-config-file-etc-default-docker

Set Docker_Opts in centos
https://stackoverflow.com/questions/26166550/set-docker-opts-in-centos

vi /etc/sysconfig/docker
    OPTIONS=--registry-mirror=https://mirror.ccs.tencentyun.com
sudo service docker restart

netstat -tnpl
CONTAINER_ID=$(sudo docker run -d -p 2222:22 rogaha/docker-desktop)

echo $(sudo docker logs $CONTAINER_ID | sed -n 1p)
User: docker Password: eengoch3ooK5
docker port $CONTAINER_ID 22

/sbin/iptables -I INPUT -p tcp --dport 80 -j ACCEPT 
/sbin/iptables -I INPUT -p tcp --dport 22 -j ACCEPT 

然后保存： 

/etc/rc.d/init.d/iptables save 
centos 5.3，5.4以上的版本需要用 
service iptables save 

人人都该学编程？
https://www.jiemodui.com/Item/22041

How to Install PHP 7 in CentOS 7
https://www.tecmint.com/install-php-7-in-centos-7/


### .vimrc

set nocp
set ts=4
set sw=4
set smarttab
set et
set ambiwidth=double
colo torte
set nu

set encoding=UTF-8
set langmenu=zh_CN.UTF-8
language message zh_CN.UTF-8
set fileencodings=ucs-bom,utf-8,cp936,gb18030,big5,euc-jp,euc-kr,latin1
set fileencoding=utf-8


syntax on
filetype plugin indent on

### .bashrc

alias rm='rm -i'
alias cp='cp -i'
alias mv='mv -i'
alias vi='vim'

# Source global definitions
if [ -f /etc/bashrc ]; then
        . /etc/bashrc
fi

export LC_ALL='zh_CN.utf8'





Programmed Lessons in QBasic
http://chortle.ccsu.edu/QBasic/index.html  发现这个 qb 教程还挺好的

Shiro的三种授权(十二)
https://www.cnblogs.com/qlqwjy/p/7257616.html
走进Java（五）JSTL和EL表达式
https://blog.csdn.net/u010096526/article/details/50038365
JSTL获取Parameter参数
https://blog.csdn.net/kevinxxw/article/details/50884649
自定义页面方法：${fns:sayHelloToName('zxw')}
https://blog.csdn.net/zhengxiangwen/article/details/40652019
JSTL表达式的使用（c:if）以及在JS中使用
https://blog.csdn.net/weistin/article/details/80027218


eclipse ERMaster插件安装 利用ERMaster快速生成db维护文档
https://my.oschina.net/dajianguo/blog/1622944    


Eclipse启动时禁用不必要的验证。
https://blog.csdn.net/u012726702/article/details/51758596

单词补全 Alt + /


window---->preferences---->general----->content types----->Text------>java properties file---->UTF-8---->update ------>ok

Mybatis整合Spring -- typeAliasesPackage
https://blog.csdn.net/sky786905664/article/details/51801933

重启 PHP-FPM

sudo kill -usr2 $(cat /var/run/php-fpm/php-fpm.pid)
查看 PHP 配置

php --ini

解决Setting property 'source' to 'org.eclipse.jst.jee.server的问题
https://blog.csdn.net/z69183787/article/details/19911935

Tomcat中server.xml配置详解
https://www.cnblogs.com/yanghua1012/p/5869192.html
tomcat context元素属性介绍
http://outofmemory.cn/code-snippet/3035/tomcat-context-element-property-introduction
tomcat 8.0特性
https://blog.csdn.net/hmy1106/article/details/51270761
Tomcat 7 的七大新特性
http://www.iteye.com/news/17928/
Tomcat 5.5.x到Tomcat 6.0（tomcat6新特性及变化）
https://blog.csdn.net/wlanye/article/details/8570891

SpringMVC重要注解（四）@ModelAttribute
https://blog.csdn.net/lovesomnus/article/details/78873089
java怎么用一行代码初始化ArrayList
https://www.itstrike.cn/Question/e74b36fa-c01f-4254-87ec-e549df2abebe.html

JS 物理引擎
Physics engine in your JavaScript program
http://slicker.me/javascript/matter.htm
黑苹果
https://github.com/kholia/OSX-KVM
命令行下的电子表格
https://github.com/andmarti1424/sc-im
A*
http://theory.stanford.edu/~amitp/GameProgramming/AStarComparison.html
可视化
https://qiao.github.io/PathFinding.js/visual/
游戏算法
https://www.redblobgames.com/
4种方法让SpringMVC接收多个对象
https://blog.csdn.net/lutinghuan/article/details/46820023
Objects binding in Spring MVC form
https://stackoverflow.com/questions/10138715/objects-binding-in-spring-mvc-form
Spring 4 官方文档学习 Web MVC 框架
https://www.cnblogs.com/t3306/p/7244134.html
Allow binding=false on @ModelAttribute
https://github.com/spring-projects/spring-framework/commit/2e7470b27f0eaae042334cd86f212cd958676be0
SpringMVC<from:form>表单标签和<input>表单标签简介
https://blog.csdn.net/hp_yangpeng/article/details/51906654
Myths about /dev/urandom
https://www.2uo.de/myths-about-urandom
With Undefined Behavior, Anything is Possible
https://raphlinus.github.io/programming/rust/2018/08/17/undefined-behavior.html
How to Read 100s of Millions of Records per Second from a Single Disk
https://clemenswinter.com/2018/08/13/how-read-100s-of-millions-of-records-per-second-from-a-single-disk/
Introduction to Go Modules
https://roberto.selbach.ca/intro-to-go-modules/

轻量级前端框架
https://mithril.js.org/

Docker的web端管理平台对比（DockerUI 、Shipyard、Portainer、Daocloud）
https://blog.csdn.net/qq273681448/article/details/75007828
Docker可视化管理工具Portainer的安装配置及使用
https://blog.csdn.net/bbwangj/article/details/80973219
Swarm -- 搭建Docker集群
https://blog.csdn.net/a632189007/article/details/78756339

How to use UTF-8 in resource properties with ResourceBundle
https://stackoverflow.com/questions/4659929/how-to-use-utf-8-in-resource-properties-with-resourcebundle
Eclipse 在线安装properties编辑插件
https://www.cnblogs.com/DylanZ/p/6428709.html


稍等两分钟，就会出现插件列表，选择PropertiesEditor，然后Next.

Where does forever store console.log output?
https://stackoverflow.com/questions/21021186/where-does-forever-store-console-log-output

forever start -o out.log -e err.log my-script.js


Learn You a Haskell for Great Good!
http://learnyouahaskell.com/chapters

owncloud+collabora 实现网盘在线预览
https://blog.csdn.net/a295184686/article/details/78632706

Epigrams on Programming
http://pu.inf.uni-tuebingen.de/users/klaeren/epigrams.html


程序员不能把自己全部的时间都用来换钱，而是要拿出20%~40%的可支配时间来学习、尝试和应用新的技术，让自己的技术栈保持连续更新。


Guacamole 通过浏览器远程访问服务器
https://www.jianshu.com/p/ebaba8ca17de

vim buffer 操作

:bn -- buffer列表中下一个 buffer　　
:bp -- buffer列表中前一个 buffer　　
:b# -- 你之前所在的前一个 buffer
:bdelete num -- 删除第num编号buffer

JavaScript Space After Function [closed]
https://stackoverflow.com/questions/9300636/javascript-space-after-function
基于Docker快速搭建多节点Hadoop集群
http://dockone.io/article/395


How to Setup Single Node Hadoop Cluster Using Docker
https://linoxide.com/cluster/setup-single-node-hadoop-cluster-docker/

A Road to Common Lisp
http://stevelosh.com/blog/2018/08/a-road-to-common-lisp/#get-a-lisp

C compiler with support for structs written in Assembly
https://news.ycombinator.com/item?id=17851311

Oops, I Wrote a C++ Compiler
https://news.ycombinator.com/item?id=17851293

Double Buffer
http://gameprogrammingpatterns.com/double-buffer.html

JSCPP, a simple C++ interpreter written in JavaScript 
https://news.ycombinator.com/item?id=17843293

Ubuntu 16.04 硬盘安装
https://www.cnblogs.com/dzlixu/p/5e9475c3990d720ca22e18b730b01d57.html


## 编程挑战

### 挑战 1：

输出 1000 以内的斐波那契数列，用空格隔开，每行 5 个显示。

### 挑战 2：

假设公司年会抽奖，一等奖1名，二等奖3名，三等奖5名，共100人抽奖，写一个抽奖程序来抽奖。
奖品不要多发，不要漏发，考虑通用性和边界处理。以后大家工作后肯定会遇到类似场景的。

### 挑战 3：

写程序解析出一个网址的各个部分

比如 https://123.abc.com:8000/hello/world?x=111&y=222&z=333 这个网址要求输出如下

协议: https
域名: 123.abc.com
端口: 8000
路径: /hello/world
参数: x: 111, y: 222, z: 333
    
### 挑战 4 ：

随机生成 100 个 15 以内的随机正整数

1、统计出每个数字出现的次数
2、统计出出现次数最多和出现次数最少的前三个数字
3、统计出偶数和奇数各自出现的次数和它们的和
4、统计出出现次数最多的偶数和奇数




## docker 常用命令


    sudo docker build -t sshd:ubuntu2 .
    sudo docker run -d --name ssh_test -p 10122:22 sshd:ubuntu2
    sudo docker run -d --name ssh_test2 -P  sshd:ubuntu3
    sudo docker commit 161f67ccad50 sshd:ubuntu
    sudo  docker exec -it b1141d7b1937 bash


    sudo /home/haohu/.local/bin/wssh --address='0.0.0.0' --port=80
    ssh root@localhost -p 10122
    
    docker run -it sequenceiq/hadoop-docker:2.7.0 /etc/bootstrap.sh -bash

    sudo docker ps -a    
    docker network create hadoop
    sudo docker-compose up -d
    sudo docker-compose stop
    sudo docker exec -it namenode bash

    hadoop fs -put /etc/issue /
    hadoop fs -ls /
    


    git pull tencent master --allow-unrelated-oo
    
    sudo docker run -d --name novnc -p 6080:80 dorowu/ubuntu-desktop-lxde-vnc
    
    sudo docker ps --filter ancestor=sshd:ubuntu2 \
        --format "table {{.ID}}\t{{.Image}}\t{{.Names}}\t{{.Status}}"
        
    sudo docker run -d -p 9000:9000     --restart=always     -v /var/run/docker.sock:/var/run/docker.sock     --name prtainer-test     docker.io/portainer/portainer
   
    docker run -m 512m --memory-swap 1G -it -p 58080:8080 --restart=always   
    --name bvrfis --volumes-from logdata mytomcat:4.0 /root/run.sh  
    docker update --restart=always xxx  
    sudo docker run --restart=on-failure:10 redis  
    
    sudo docker swarm init --advertise-addr 192.168.1.15
    docker swarm join-token worker
    docker swarm join --token SWMTKN-1-2nifhbsha6kzfu7pacy93z1niki425t2f3t807y1kzehxhsval-5zns821bezcby2k1o0v7y946z 192.168.1.15:2377
    sudo docker node ls
    
    sudo docker service create --replicas 1 --name hadoop-test01 sequenceiq/hadoop-docker /etc/bootstrap.sh
    sudo docker service ps hadoop-test01
    sudo docker service inspect --pretty hadoop-test01
    docker service scale helloworld=2
    sudo docker service rm hadoop-test01
    
    docker swarm leave
    
    sudo docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' ssh.1.uoyp9smajh939e98yc40ygm5z



sudo sed -i "s|EXTRA_ARGS='|EXTRA_ARGS='--registry-mirror=http://1d20ae13.m.daocloud.io |g" /var/lib/boot2docker/profile    

Docker(六)：Docker 三剑客之 Docker Swarm
https://baijiahao.baidu.com/s?id=1598047425152066542&wfr=spider&for=pc

Docker Swarm 部署Mysql/Mariadb高可用主从复制集群
http://www.chairis.cn/blog/article/90

docker 容器日志清理方案
http://www.chairis.cn/blog/article/94
    
docker应用-5（使用overlay 网络进行容器间跨物理主机通信）
https://www.jianshu.com/p/4bbaf761fad8

Docker Swarm集群部署实践
http://www.chairis.cn/blog/article/89    

        
在使用docker run启动容器时，使用--restart参数来设置：        
--restart具体参数值详细信息：
no -  容器退出时，不重启容器；
on-failure - 只有在非0状态退出时才从新启动容器；
always - 无论退出状态是如何，都重启容器；

Docker容器开机自动启动
https://blog.csdn.net/menghuanbeike/article/details/79261828

使用DockerToolbox自动创建Swarm集群+Portainer图形化管理的脚本
https://blog.csdn.net/CSDN_duomaomao/article/details/73430919

Docker-Hadoop ALL-IN-ONE
https://www.jianshu.com/p/6bcd72083c08

    
    
Docker Container Executor
https://hadoop.apache.org/docs/r2.7.2/hadoop-yarn/hadoop-yarn-site/DockerContainerExecutor.html
Docker image for Hadoop
https://github.com/bigdatafoundation/docker-hadoop    

使用Docker在本地搭建Hadoop分布式集群
https://www.cnblogs.com/onetwo/p/6419925.html
将Linux系统的home、var目录迁移到新分区
https://blog.csdn.net/davidhopper/article/details/79768073
How do I change the Docker image installation directory?
https://forums.docker.com/t/how-do-i-change-the-docker-image-installation-directory/1169
关于docker的15个小tip
http://www.cnblogs.com/elnino/p/3899136.html
运行 MapReduce 样例
https://blog.csdn.net/chengqiuming/article/details/78826143

Docker环境下Hadoop分布式集群搭建
https://blog.csdn.net/zhangfan1212/article/details/54791334

Docker-Hadoop ALL-IN-ONE
https://www.jianshu.com/p/6bcd72083c08
Docker创建私有仓库+SSL+AUTH+WEB
https://www.jianshu.com/p/d85398240f05
Docker-Compose入门
https://blog.csdn.net/chinrui/article/details/79155688
使用docker部署hadoop hdfs
http://fatkun.com/2017/12/deploy-hadoop-hdfs-use-docker.html

Docker Machine 是什么？
https://www.cnblogs.com/sparkdev/p/7044950.html





http://npm.taobao.org/mirrors/chromedriver/
v2.40 Supports Chrome v66-68
http://npm.taobao.org/mirrors/chromedriver/2.40/notes.txt

Windows下的Jupyter Notebook 安装与自定义启动（图文详解）
http://www.cnblogs.com/zlslch/p/6984403.html

pip install selenium

Python3.5+selenium操作Chrome浏览器
https://www.cnblogs.com/drake-guo/p/6188366.html

selenium 安装与 chromedriver安装
https://www.cnblogs.com/technologylife/p/5829944.html

最详尽使用指南：超快上手Jupyter Notebook
https://blog.csdn.net/DataCastle/article/details/78890469

Python+Selenium WebDriver API：浏览器及元素的常用函数及变量整理总结
https://www.cnblogs.com/yufeihlf/p/5764807.html

mkdir ~/.pip/

vi ~/.pip/pip.conf

    [global]
    index-url = https://pypi.tuna.tsinghua.edu.cn/simple
    [install]
    trusted-host=mirrors.aliyun.com
    
pip install virtualenv
virtualenv venv
echo venv >> .gitignore

pip install Flask
pip install docker
pip freeze > requirements.txt

mkdir static
mkdir templates

. venv/bin/activate
export FLASK_ENV=development
export FLASK_APP=dockerweb.py
flask run --host=0.0.0.0

wssh 目录
/home/haohu/.local/lib/python2.7/site-packages/webssh
wssh debug 模式会去掉 csrf 
sudo /home/haohu/.local/bin/wssh --address='0.0.0.0' --port=8000 --debug=true   

screen -dmS dockerweb
screen -r dockerweb


8天学会Hadoop
https://ke.qq.com/course/229879
https://ke.qq.com/course/276816
https://ke.qq.com/course/287048


GRANT ALL PRIVILEGES ON techaction.* TO 'root'@'%' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON techaction.* TO 'root'@'localhost' IDENTIFIED BY 'password';
GRANT SELECT ON *.* TO 'readonly'@'localhost' IDENTIFIED BY 'readonly';
flush privileges;

mysql添加用户、修改权限，修改登录权限ip
https://www.cnblogs.com/lemon-flm/p/7597879.html

An Introduction to Modern CMake
https://cliutils.gitlab.io/modern-cmake/

PDF 转换
https://www.ilovepdf.com/

sudo apt-get update
sudo apt-get upgrade

（实用）Ubuntu 、CentOS更换国内源
https://www.cnblogs.com/Security-Darren/p/3947952.html



curl -o /dev/null -s -w 'status=%{http_code}\ndns-time=%{time_namelookup}s\nconnec-time=%{time_connect}s\nserver-time=%{time_starttransfer}s\ntota-ltime=%{time_total}\ncontent-length=%{size_download}\n' http://techaction.cn






function reserved_ip($ip)
{
    $reserved_ips = array( // not an exhaustive list
    '167772160'  => 184549375,  /*    10.0.0.0 -  10.255.255.255 */
    '3232235520' => 3232301055, /* 192.168.0.0 - 192.168.255.255 */
    '2130706432' => 2147483647, /*   127.0.0.0 - 127.255.255.255 */
    '2851995648' => 2852061183, /* 169.254.0.0 - 169.254.255.255 */
    '2886729728' => 2887778303, /*  172.16.0.0 -  172.31.255.255 */
    '3758096384' => 4026531839, /*   224.0.0.0 - 239.255.255.255 */
    );

    $ip_long = sprintf('%u', ip2long($ip));

    foreach ($reserved_ips as $ip_start => $ip_end)
    {
        if (($ip_long >= $ip_start) && ($ip_long <= $ip_end))
        {
            return TRUE;
        }
    }
    return FALSE;
}

var_dump(reserved_ip('127.0.0.1')); // reserved (localhost)
var_dump(reserved_ip('74.125.140.101')); // not reserved (Google)


iView 发布 3.0 版本，以及开发者社区等 5 款新产品
https://www.v2ex.com/t/475227#reply10

git config --global core.editor vim
git config --global core.autocrlf true
git config --global core.safecrlf true


sudo su
mkdir /data/bakup
mysqldump -uroot -p --all-databases >/data/bakup/dump-`date +%Y%m%d%H%M%S`.sql

Can I restore a single table from a full mysql mysqldump file?
https://stackoverflow.com/questions/1013852/can-i-restore-a-single-table-from-a-full-mysql-mysqldump-file

腾讯工程师带你深入解析 MySQL binlog
https://zhuanlan.zhihu.com/p/33504555


ubuntu开启crontab日志记录及解决No MTA installed, discarding output问题
http://www.pooy.net/ubuntu-open-crontab-logging-and-resolution-no-mta-installed-discarding-output-problem.html

ERROR: Failed to allocate directory watch: Too many open files
sysctl fs.inotify.max_user_instances=512


解决(CRON) info (No MTA installed, discarding output)
https://blog.csdn.net/win_turn/article/details/53000899


像素
https://art.pixlab.io/#picLoader

linux系统挂载U盘，中文文件名乱码解决方案
https://www.cnblogs.com/zhouqinxiong/p/3497293.html

Linux下添加新硬盘,分区及挂载
https://www.cnblogs.com/jiu0821/p/7209825.html

挂载 U 盘
mount -o iocharset=utf8 /dev/sdb4 /mnt

## 分区

    # 查看分区表，/dev/sda，/dev/sdb 表示硬盘，/dev/sda1, /dev/sda2 表示分区
    fdisk -l |grep '/dev/sd[abcd]'
    
    # 对 /dev/sdb 分区
    fdisk /dev/sdb

    # 添加新分区
    n
    
    # e 为扩展分区， p 为主分区
    p
    
    # 确认分区起始点，如果是新硬盘，输入 1，一般情况下直接回车
    1
    
    #输入分区大小，以下表示 1G，注意 m 是小写
    +1024m
    
    # 保存分区
    w
    
    # 查看新分好的区
    fdisk -l
    
    # 格式化
    mkfs -t ext4 -c /dev/sdb1
    
    # 挂载
    mount /dev/sdb1 /www
    
    # 查看挂载的分区大小
    df -TH
    
    # 设置为开机自动挂载
    echo '/dev/sdb1 /www ext4 defaults 1 2' >> /etc/fstab
    

导出镜像
docker save -o vnc.tar vnc:0.01    
    
查看磁盘 IO    
iostat -d -x -k 1 | grep -E '(Device|sd[abcd])'


docker镜像的导入和导出
https://blog.csdn.net/x6_9x/article/details/72891404 


彻底禁用Chrome的“请停用以开发者模式运行的扩展程序”提示
提示
https://www.cnblogs.com/liuxianan/p/disable-chrome-extension-warning.html 真够复 真够复杂的



## 重装系统

备份

- chrome 收藏夹
- putty 配置
- git key


至强CPU多数都是可以配置多路的，就是多个CPU放在同一个板子上，这一点是i7无法做到的。
至强E5系列里，四位数字的第一位表示的就是CPU的个数，比如Xeon E5-2696 v3，表示此款CPU支持双路，
Xeon E5-4655 v3支持四路，那么我给的列表里E5最高配置是Xeon E5-4669 v3，四路，每路18核，每核双线程，
那么要组装到板子上，在Windows任务管理器里就可以看到壮观的144个核心的场面，

Intel超级大杀器发布:28核56线程桌面CPU,4.3G还不锁频
http://diy.pconline.com.cn/1180/11808584.html

ubuntu16.04开机启动字符界面
https://jingyan.baidu.com/article/948f5924ee2a5dd80ff5f9e4.html

非常实用的Linux 系统监控工具
https://www.cnblogs.com/mengdeep/p/5296991.html

了解VMware预订限制和共享
Understanding VMware Reservations Limits and Shares
http://www.vfrank.org/2013/09/19/understanding-vmware-reservations-limits-and-shares/

Docker: 限制容器可用的内存
http://www.cnblogs.com/sparkdev/p/8032330.html

Docker service Limits and Reservations
https://stackoverflow.com/questions/38200028/docker-service-limits-and-reservations

浮点算法
echo "scale=2;$a/$b" | bc


Swarm mode: Inspect worker node's container on manager node
https://stackoverflow.com/questions/39237998/swarm-mode-inspect-worker-nodes-container-on-manager-node


Error loading config file XXX.dockerconfig.json permission denied
https://blog.csdn.net/xukai0110/article/details/80637884

sudo chown "$USER":"$USER" /home/"$USER"/.docker -R
sudo chmod g+rwx "/home/$USER/.docker" -R

How can I use docker without sudo?
https://askubuntu.com/questions/477551/how-can-i-use-docker-without-sudo

sudo groupadd docker
sudo gpasswd -a $USER docker
newgrp docker
docker ps

How to determine where an environment variable came from
https://unix.stackexchange.com/questions/813/how-to-determine-where-an-environment-variable-came-from


ubuntu 死机，查看日志


Linux Kernel panic issue: How to fix hung_task_timeout_secs and blocked for more than 120 seconds problem
https://www.blackmoreops.com/2014/09/22/linux-kernel-panic-issue-fix-hung_task_timeout_secs-blocked-120-seconds-problem/


NO-BREAK SPACE
https://stackoverflow.com/questions/5237989/nonbreaking-space


VNC Tight Encoder - Comparison Results
http://tightvnc.com/archive/compare.html

Comparing 7 Monitoring Options for Docker
https://rancher.com/comparing-monitoring-options-for-docker-deployments/


一种基于负载预测的DockerSwarm集群资源调度优化方法与流程
http://www.xjishu.com/zhuanli/55/201710461892.html

运维之我的docker-集群的管理-swarm
http://blog.51cto.com/nginxs/1894432

Docker Stack Swarm - Service Replicas are not spread for Mutli Service Stack
https://stackoverflow.com/questions/44868123/docker-stack-swarm-service-replicas-are-not-spread-for-mutli-service-stack


https://www.cnblogs.com/aguncn/p/6904522.html

清理Docker占用的磁盘空间
https://blog.csdn.net/weixin_32820767/article/details/81196250

Docker网络和 overlay跨主机通讯
http://blog.51cto.com/littledevil/1922922

Docker Swarm 入门：Service Network 管理
https://www.jianshu.com/p/60bccbdb6af9


Battlefield: Calico, Flannel, Weave and Docker Overlay Network
http://xelatex.github.io/2015/11/15/Battlefield-Calico-Flannel-Weave-and-Docker-Overlay-Network/


Demystifying Docker overlay networking
http://blog.nigelpoulton.com/demystifying-docker-overlay-networking/

DOCKER_OPTS do not work in config file /etc/default/docker
https://stackoverflow.com/questions/27763340/docker-opts-do-not-work-in-config-file-etc-default-docker

journalctl -xe

金步国作品集 各种手册翻译
http://www.jinbuguo.com/

分页无截断查看日志
journalctl -rxn -u docker.service | less
查看错误日志
journalctl -p err..alert
查看内核日志
journalctl -k
显示本次启动后的所有日志：
journalctl -b

journalctl: how to prevent text from truncating in terminal
https://unix.stackexchange.com/questions/229188/journalctl-how-to-prevent-text-from-truncating-in-terminal

systemd 之 journalctl
https://www.cnblogs.com/itxdm/p/Systemd_log_system_journalctl.html

Systemd 常规操作与彩蛋
http://www.cnblogs.com/itxdm/p/Systemd_regular_operation_with_eggs.html


DOCKER图形页面管理工具--3种，shipyard最强大，其次是portainer
https://blog.csdn.net/xl_lx/article/details/81183956

Protect the Docker daemon socket
docker 进程认证
https://docs.docker.com/engine/security/https/

Docker security 安全
https://docs.docker.com/engine/security/security/#kernel-namespaces


 算机专业课一体化支撑平台 北航 CG OJ
http://www.cjudge.net/FAQs.html

linux开发神器--Tmux
https://www.cnblogs.com/ArsenalfanInECNU/p/5756763.html


tmux new -s monitor

按下 Ctrl-b 后的快捷键如下：


% 创建一个水平窗格
" 创建一个竖直窗格
方向键切换窗格
q 显示窗格的编号
o 在窗格间切换
ctrl + 方向键， alt + 方向键，切换大小
b 离开会话，然后可以用 tmux attach 挂载
x 关闭当前窗格

node js 进程守护神forever
https://blog.csdn.net/jbboy/article/details/35281225

apt-cache show xserver-xorg | grep Version
https://superuser.com/questions/366505/how-to-find-out-xorg-version-or-whats-my-xorg-version

htop 快捷键，H 切换用户线程 K 切换内核线程

Why docker uses port numbers from 32768-65535?
https://stackoverflow.com/questions/40787524/why-docker-uses-port-numbers-from-32768-65535

容器删除后，主机映射给容器的端口为何并立即未回收利用？
https://segmentfault.com/q/1010000000496866

NGINX as a WebSocket Proxy
https://www.nginx.com/blog/websocket-nginx/


Ganglia 权威指南-安装Ganglia过程
http://www.cnblogs.com/chris-cp/p/4324392.html



第2章 rsync(一)：基本命令和用法
https://www.cnblogs.com/f-ck-need-u/p/7220009.html

rsync -avP /var/www/html/ action@192.168.1.102:/var/www/html


Eclipse快捷键 10个最有用的快捷键
https://blog.csdn.net/lynn349x/article/details/56282704

How to convert an rtf string to text in C#
https://stackoverflow.com/questions/5634525/how-to-convert-an-rtf-string-to-text-in-c-sharp

grep 和 awk的buffer
https://blog.csdn.net/csCrazybing/article/details/78096301

How to fix stdio buffering
http://www.perkin.org.uk/posts/how-to-fix-stdio-buffering.html


Bash History Display Date And Time For Each Command
https://www.cyberciti.biz/faq/unix-linux-bash-history-display-date-time/


hadoop 集群 硬件配置
http://info.ipieuvre.com/article/201506/250.html
https://www.oschina.net/translate/how-to-select-the-right-hardware-for-your-new-hadoop-cluster

Docker 日志都在哪里？怎么收集？
https://www.cnblogs.com/YatHo/p/7866029.html

PHP file_get_contents fails to read zip on windows
https://stackoverflow.com/questions/27405430/php-file-get-contents-fails-to-read-zip-on-windows

baidu ai studio
http://aistudio.baidu.com/#/projectDetail/35620

百度实验平台
http://abcinstitute.baidu.com/lab/experiment/list;JSESSIONID=d8d1ce38-2afe-4324-b976-2f908f9dea15

机器学习——15分钟透彻理解感知机
https://blog.csdn.net/yxhlfx/article/details/79093456

自然语言处理 中文分词 词性标注 命名实体识别 依存句法分析 新词发现 关键词短语提取 自动摘要 文本分类聚类 拼音简繁
https://github.com/hankcs/HanLP#1-%E7%AC%AC%E4%B8%80%E4%B8%AAdemo

搜狗实验室
http://www.sogou.com/labs/

word2vec原理推导与代码分析
http://www.hankcs.com/nlp/word2vec.html

识别数字
http://www.paddlepaddle.org/documentation/docs/zh/develop/beginners_guide/quick_start/recognize_digits/README.cn.html

PaddlePaddle  新手入门
http://www.paddlepaddle.org/documentation/docs/zh/1.2/beginners_guide/index.html

Deep Learning（深度学习） 中文版
https://github.com/exacity/deeplearningbook-chinese

神经网络的四块积木：全连接，激活函数，卷积，池化
三种神经网络模型：Softmax回归模型，多层感知机模型，卷积神经网络模型
LeNet-5

三分钟带你对 Softmax 划重点
https://blog.csdn.net/red_stone1/article/details/80687921
小白都能看懂的softmax详解
https://blog.csdn.net/bitcarmanlee/article/details/82320853

Istio是啥？一文带你彻底了解！
https://www.sohu.com/a/270131876_463994

nginx配合modsecurity实现WAF功能
https://www.52os.net/articles/nginx-use-modsecurity-module-as-waf.html
https://www.techrepublic.com/article/how-to-install-and-enable-modsecurity-with-nginx-on-ubuntu-server/
CentOS Linux下用Nginx和Naxsi搭建Web应用防火墙
http://blog.cnwyhx.com/centos-nginx-naxsi-install/
nginx下安装配置naxsi waf防火墙（附完整编译、配置）
http://f2ex.cn/nginx-installed-configuration-naxsi-waf/

nginx的sql注入过滤配置
http://blog.itpub.net/30208512/viewspace-1578399/

Nginx 配置格式化小工具
https://github.com/fangpeishi/ngxfmt

轻松玩转OpenWAF之安装篇.md
https://github.com/titansec/OpenWAF/blob/master/doc/%E8%BD%BB%E6%9D%BE%E7%8E%A9%E8%BD%ACOpenWAF%E4%B9%8B%E5%AE%89%E8%A3%85%E7%AF%87.md

How to install and enable ModSecurity with NGINX on Ubuntu Server
https://www.techrepublic.com/article/how-to-install-and-enable-modsecurity-with-nginx-on-ubuntu-server/


Compatibility of ModSecurity with NginX waf
https://stackoverflow.com/questions/44978041/compatibility-of-modsecurity-with-nginx


2018-12-27T16:45:54+08:00 404 0.000 - 119.180.52.108 "POST /admin/login HTTP/1.1" 571 "http://techaction.cn/admin/login" "Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/69.0.3497.100 Safari/537.36" "-"


2018/12/27 16:46:52 [error] 9952#0: *132 open() "/data/release/ytaction/src/public/admin/login" failed (2: No such file or directory), client: 119.180.52.108, server: techaction.cn, request: "POST /admin/login HTTP/1.1", host: "techaction.cn", referrer: "http://techaction.cn/admin/login"


How to Install Nginx with libModSecurity and OWASP core rule set on Ubuntu 16
https://www.hugeserver.com/kb/install-nginx-libmodsecurity-owasp-core-ruleset-ubuntu16/

Ubuntu 16.04上使用libmodsecurity的Nginx和OWASP ModSecurity核心规则
https://www.howtoing.com/nginx-with-libmodsecurity-and-owasp-modsecurity-core-rule-set-on-ubuntu-1604/

How to Install libmodsecurity + nginx on Ubuntu 14.04
https://help.dreamhost.com/hc/en-us/articles/223608748-How-to-Install-libmodsecurity-Nginx-on-Ubuntu-14-04


斯坦福大学公开课 ：机器学习课程
http://open.163.com/special/opencourse/machinelearning.html
百度 AI 课程
https://ai.baidu.com/paddlepaddle/player?id=13



Cleaning up docker to reclaim disk space
https://lebkowski.name/docker-volumes/

#!/bin/bash

    # remove exited containers:
    docker ps --filter status=dead --filter status=exited -aq | xargs -r docker rm -v

    # remove unused images:
    docker images --no-trunc | grep '<none>' | awk '{ print $3 }' | xargs -r docker rmi

    # remove unused volumes (needs to be ran as root):
    find '/var/lib/docker/volumes/' -mindepth 1 -maxdepth 1 -type d | grep -vFf <(
      docker ps -aq | xargs docker inspect | jq -r '.[]|.Mounts|.[]|.Name|select(.)'
    ) | xargs -r rm -fr
    
    
    
CREATE DATABASE IF NOT EXISTS techaction default charset utf8 COLLATE utf8_general_ci; 

Windows远程数据同步工具cwRsync
https://www.cnblogs.com/l1pe1/p/4901031.html

Netplan – How To Configure Static IP Address in Ubuntu 18.04 using Netplan
https://www.itzgeek.com/how-tos/linux/ubuntu-how-tos/netplan-how-to-configure-static-ip-address-in-ubuntu-18-04-using-netplan.html

apt 下载
sudo apt-get install -d  network-manager
apt-offline - offline apt package manager
apt-zip - Update a non-networked computer using apt and removable media
apt download <package_name>

https://stackoverflow.com/questions/4419268/how-do-i-download-a-package-from-apt-get-without-installing-it

https://blog.csdn.net/thinktalk/article/details/83716617

Ubuntu中启用关闭Network-manager网络设置问题
https://blog.csdn.net/weixin_42155195/article/details/80683166

如何在 Linux 上使用网络配置工具 Netplan
https://linux.cn/article-10095-1.html?pr

ubuntu使用apt-get制作OfflinePackage
https://blog.csdn.net/ouyangziling/article/details/79056161


rsync也可以通过校验和比较文件。

--size-only这意味着rsync将跳过大小匹配的文件，即使时间戳不同。这意味着它将同步比默认行为更少的文件

--ignore-times 这意味着rsync将检查每个文件的和，即使时间戳和文件大小匹配。这意味着它将同步比默认行为更多的文件。


rsync “Operation not permitted”
https://serverfault.com/questions/296587/rsync-operation-not-permitted

函数响应式编程（FRP）思想
https://blog.csdn.net/fly1183989782/article/details/62053973

漫谈FRP之 其实你早就学过FRP
http://insights.thoughtworkers.org/frp-series-0-not-new-concept/

函数编程中functor和monad的形象解释
https://www.jdon.com/idea/functor-monad.html

bootstrap dropdown hover menu
https://codepen.io/bsngr/pen/frDqh

How to create a collapsing tree table in html/css/js?  树形结构
https://stackoverflow.com/questions/5636375/how-to-create-a-collapsing-tree-table-in-html-css-js

chrome插件 —— 帮助高度还原设计稿
https://www.cnblogs.com/joyho/articles/5622760.html

OpenPAI：大规模人工智能集群管理平台
https://www.msra.cn/zh-cn/news/features/openpai


Cython入门到放弃（一）
https://blog.csdn.net/qtlyx/article/details/80614608

Best approach to encrypt big files with php
https://stackoverflow.com/questions/16175154/best-approach-to-encrypt-big-files-with-php

加密解密
Whole File Encryption/Decryption With PHP
http://monkeylogic.com/whole-file-encryptiondecryption-with-php/

All the crypto code you’ve ever written is probably broken
https://tonyarcieri.com/all-the-crypto-code-youve-ever-written-is-probably-broken

openssl -aes-128-ecb encryption doesn't match python Crypto.Cipher AES encryption
https://stackoverflow.com/questions/48410452/openssl-aes-128-ecb-encryption-doesnt-match-python-crypto-cipher-aes-encryptio

A Python-to-PHP compatible AES encryption with openssl_encrypt AES-CBC
https://stackoverflow.com/questions/40820661/a-python-to-php-compatible-aes-encryption-with-openssl-encrypt-aes-cbc

PHP 加密，Python 解密
A Python-to-PHP compatible AES encryption with openssl_encrypt AES-CBC
https://stackoverflow.com/questions/40820661/a-python-to-php-compatible-aes-encryption-with-openssl-encrypt-aes-cbc

云脑科技徐昊：AutoML 工程实践与大规模行业应用
http://www.lyweixiao.com/5314124/20190105A0YCBV00.html

https://serverfault.com/questions/870568/fatal-error-cant-open-and-lock-privilege-tables-table-storage-engine-for-use
Fatal error: Can't open and lock privilege tables: Table storage engine for 'user' doesn't have this option

Docker CPU 资源限制——CPU固定核功能测试
https://www.cnblogs.com/zhenyuyaodidiao/p/5061884.html

Linux下限制进程的CPU利用率
https://blog.csdn.net/bailyzheng/article/details/51355384

Linux---使用 nice、cpulimit 和 cgroups 限制 cpu 占用率
https://blog.csdn.net/loyachen/article/details/52167124

How do I install Ubuntu Server (step-by-step)?
https://askubuntu.com/questions/340965/how-do-i-install-ubuntu-server-step-by-step

H5 游戏引擎
 phaser，pixi，enchant.js

【blockly教程】第一章 Google Blockly教学应用手册
https://www.cnblogs.com/scratch8/archive/2018/09/12/9637214.html
https://www.cnblogs.com/scratch8/category/1299483.html
https://v.youku.com/v_show/id_XMTg3MTYzNjYzNg==.html
https://blog.csdn.net/oalevel/article/details/81834837


用友T3
http://www.3322.cc/soft/43731.html

Redis 设计与实现¶
http://redisbook.com/index.html

技术图书作译者的炼成方法
http://blog.huangz.me/2017/how-i-became-a-writer-and-translator.html

《Redis in Action》翻译记事
http://blog.huangz.me/diary/2015/memories-of-redis-in-action-translation.html

分布式监控工具Ganglia 介绍 与 集群部署.
https://www.cnblogs.com/yuki-lau/p/3201110.html 

数据可视化（三）基于 Graphviz 实现程序化绘图
https://riboseyim.com/2017/09/15/Visualization-Graphviz/

全面学习Prometheus
https://www.sohu.com/a/233111809_198222

Cacti：cacti是用php语言实现的一个软件，它的主要功能是用snmp服务获取数据，然后用rrdtool储存和更新数据，当用户需要查看数据的时候用rrdtool生成图表呈现给用户。
Nagios：Nagios 利用其众多的插件实现对本机和远端服务的监控，当被监控对象出现异常，Nagios 就会及时给管理人员告警。
Graphite：Graphite 是处理可视化和指标数据的优秀开源工具。它有强大的查询 API 和相当丰富的插件功能设置。

Kibana：Kibana是一个针对Elasticsearch的开源分析及可视化平台，用来搜索、查看交互存储在Elasticsearch索引中的数据
Grafana：Grafana是一个跨平台的开源的度量分析和可视化工具，可以通过将采集的数据查询然后可视化的展示，并及时通知

Zabbix：zabbix 是一个基于WEB界面的提供分布式系统监视以及网络监视功能的企业级的开源解决方案
Ganglia：Ganglia是UC Berkeley发起的一个开源集群监视项目，设计用于测量数以千计的节点。
Prometheus：Prometheus 将所有信息都存储为时间序列数据，实时分析系统运行的状态、执行时间、调用次数等，以找到系统的热点，为性能优化提供依据。


通过建立完善的监控体系，从而达到以下目的：

长期趋势分析：通过对监控样本数据的持续收集和统计，对监控指标进行长期趋势分析。例如，通过对磁盘空间增长率的判断，我们可以提前预测在未来什么时间节点上需要对资源进行扩容。
对照分析：两个版本的系统运行资源使用情况的差异如何？在不同容量情况下系统的并发和负载变化如何？通过监控能够方便的对系统进行跟踪和比较。
告警：当系统出现或者即将出现故障时，监控系统需要迅速反应并通知管理员，从而能够对问题进行快速的处理或者提前预防问题的发生，避免出现对业务的影响。
故障分析与定位：当问题发生后，需要对问题进行调查和处理。通过对不同监控指标以及历史数据的分析，能够找到并解决根源问题。
数据可视化：通过可视化仪表盘能够直接获取系统的运行状态、资源使用情况、以及服务运行状态等直观的信息。


elk
日志存几天，可以按天分区的，定时删
其它运维指标和运营指标存的时间比较久
单元测试和拨测成功率都扔es里，每天发报表到小组邮件里
还有每天的 Error 日志 loggerName， 慢速 api，慢速 sql 的top 10
每个规模指标，收入指标，LoggerName，API 性能，慢 SQL 都有对应负责人
日志组件是 error 日志 es, db，本机文本都记一份，warning 日志只记 es 和 本机文本，debug 只记录到本机
查问题先查 db，然后es，最后写了个分布式 grep  可以在web界面上对多台机器上同时进行 grep，前提是每台机器的日志的相对路径是一样的，而且使用者在cmdb里有这几台机器的权限。


【技能】小白耳机维修入门--各种耳机插头接线图--耳机维修汇总贴
https://www.cnblogs.com/tony-ning/p/7445761.html

科普帖：深度学习中GPU和显存分析
https://blog.csdn.net/liusandian/article/details/79069926
深度学习需要的显卡配置
https://blog.csdn.net/pjh23/article/details/83513066
【深度学习】为什么深度学习需要大内存？
https://blog.csdn.net/shenxiaolu1984/article/details/71522141

Docker环境下玩转GPU(一)
https://www.jianshu.com/p/2442394a934e?utm_campaign=maleskine&utm_content=note&utm_medium=seo_notes&utm_source=recommendation

ML之NN：BP solve XOR Problem
https://blog.csdn.net/qq_41185868/article/details/80789982
【机器学习】神经网络实现异或（XOR）
http://www.cnblogs.com/Belter/p/6711160.html

不用算术运算符实现两个数的加法(按位异或)
http://www.cnblogs.com/houjun/p/4908725.html


Codeup墓地 Online Judge FAQ
http://codeup.cn/faqs.php
OnlineJudge 2.0
https://github.com/QingdaoU/OnlineJudge/blob/master/README-CN.md
模型评估指标AUC（area under the curve）
https://blog.csdn.net/liweibin1994/article/details/79462554


获取 group by 后的序号，第几组的第几条数据：
        
SELECT 
@exp_number:=CASE WHEN @task_id=task_id THEN @exp_number+1 ELSE 1 END AS exp_number,
@task_number:=CASE WHEN @exp_number = 1 THEN @task_number+1 ELSE @task_number END AS task_number,
@task_id:=task_id AS task_id,
CONCAT(@task_number, '.', @exp_number) AS seq,
exp_id
FROM exp_course_class,(SELECT @task_number:=0, @exp_number:=0,@task_id:='') AS t
WHERE course_id = 41 AND class_id = 40 GROUP BY  task_id, pos, exp_id 
ORDER BY task_id, pos, task_number, exp_number;       

线性代数——向量、向量加法、向量数乘
https://blog.csdn.net/Fancy_Real/article/details/79944916
线性代数的本质学习笔记（1）：向量、线性组合、张成（SPAN）、线性变换
https://blog.csdn.net/dugudaibo/article/details/78714668

矩阵-DirectX与OpenGL的不同
http://www.cnblogs.com/graphics/archive/2012/08/02/2616017.html

## 数学
物理专业：向量是空间中的箭头，由长度和方向决定。可以自由移动；数学专业：向量可以是任何东西，只保证向量加法和数乘运算有意义；计算机专业：向量是有序的数字列表，起始点在原点上。

所有可以表示为给定向量线性组合的向量集合被称为给定向量张成的空间。

两个向量在三维空间中往往构成的是一个平面，有的时候也可能是一个直线。三个向量一般在三维空间中张成了整个三维空间，可以想象一下，两个向量已经张成了一个平面，而平面沿着第三个向量进行平移，张成了整个三维空间。新增的向量如果落在了原有向量张成的空间中，那么这个向量与原先的向量是线性相关的；另一方面如果所有向量都给张成的空间增添了新的维度，它们就是线性无关的。

向量在右 矩阵在左的时候

线性变换就是把矩阵里的值看成列向量

空间投影就是把矩阵看成行向量（每个行向量和右边向量点积，点积即投影）

首先，线性变换是把一个向量变为另一个向量，这里不涉及坐标变换。形式上，你可以把向量写成一行，然后右边乘一个矩阵，结果仍然写成了一行，成为新的向量。至于向量左乘矩阵，当这个向量的每个分量都表示一个基的时候，这就是基变换；而当这个向量的每个分量只是向量分量时，这就是线性变换。

线性组合 线性变换 线性相关 线性可分 空间投影

OpenGL中经常会使用的平移矩阵、缩放矩阵以及旋转矩阵，投影矩阵。

解析解，是指通过严格的公式所求得的解。即包含分式、三角函数、指数、对数甚至无限级数等基本函数的解的形式。给出解的具体函数形式，从解的表达式中就可以算出任何对应值。用来求得解析解的方法称为解析法，解析法是常见的微积分技巧，如分离变量法等。解析解为一封闭形式的函数，因此对任一独立变量，皆可将其代入解析函数求得正确的相依变量。因此，解析解也称为闭式解。

特别的，凸集，实数R上（或复数C上）的向量空间中，如果集合S中任两点的连线上的点都在S内，则称集合S为凸集。

凸函数是一个定义在某个向量空间的凸子集C（区间）上的实值函数f，而且对于凸子集C中任意两个向量  , f((x1+x2)/2)>=(f(x1)+f(x2))/2,则f(x)是定义在凸子集c中的凸函数（该定义与凸规划中凸函数的定义是一致的，下凸）。

牛顿法是一种在实数域和复数域上近似求解方程的方法。方法使用函数f(x)的泰勒级数的前面几项来寻找方程f(x) = 0的根。牛顿法最大的特点就在于它的收敛速度很快。

梯度下降法实现简单，当目标函数是凸函数时，梯度下降法的解是全局解。一般情况下，其解不保证是全局最优解，梯度下降法的速度也未必是最快的。梯度下降法的优化思想是用当前位置负梯度方向作为搜索方向，因为该方向为当前位置的最快下降方向，所以也被称为是”最速下降法“。

梯度的本意是一个向量（矢量），表示某一函数在该点处的沿着该方向取得最大值，即函数在该点处沿着该方向（此梯度的方向）变化最快，变化率最大（为该梯度的模）。

在函数定义域的内点，对某一方向求导得到的导数。一般为二元函数和三元函数的方向导数，方向导数可分为沿直线方向和沿曲线方向的方向导数。

启发式优化方法种类繁多，包括经典的模拟退火方法、遗传算法、蚁群算法以及粒子群算法等等。

共轭梯度法是介于最速下降法与牛顿法之间的一个方法，它仅需利用一阶导数信息，但克服了最速下降法收敛慢的缺点，又避免了牛顿法需要存储和计算Hesse矩阵并求逆的缺点，共轭梯度法不仅是解决大型线性方程组最有用的方法之一，也是解大型非线性最优化最有效的算法之一。

共轭在数学、物理、化学、地理等学科中都有出现。 本意：两头牛背上的架子称为轭，轭使两头牛同步行走。共轭即为按一定的规律相配的一对。通俗点说就是孪生。

作为一种优化算法，拉格朗日乘子法主要用于解决约束优化问题，它的基本思想就是通过引入拉格朗日乘子来将含有n个变量和k个约束条件的约束优化问题转化为含有（n+k）个变量的无约束优化问题。拉格朗日乘子背后的数学意义是其为约束方程梯度线性组合中每个向量的系数。

最优化问题的共同特点是：求满足一定条件的变量x1，x2，…，xn，使某函数f(x1，x2，…，xn)取得最大值或者最小值。

矩阵A为n阶方阵，若存在n阶矩阵B，使得矩阵A、B的乘积为单位阵，则称A为可逆阵，B为A的逆矩阵。若方阵的逆阵存在，则称为可逆矩阵或非奇异矩阵，且其逆矩阵唯一。
在矩阵的乘法中，有一种矩阵起着特殊的作用，如同数的乘法中的1，这种矩阵被称为单位矩阵。它是个方阵，从左上角到右下角的对角线（称为主对角线）上的元素均为1。除此以外全都为0。

矩阵求导（Matrix Derivative）也称作矩阵微分（Matrix Differential），在机器学习、图像处理、最优化等领域的公式推导中经常用到。

矩阵的微积分本质上是多元变量的微积分问题，只是应用在矩阵空间上而已

机器学习中的线性代数之矩阵求导
https://blog.csdn.net/u010976453/article/details/54381248

参数估计是机器学习里面的一个重要主题，而极大似然估计是最传统、使用最广泛的估计方法之一。

十分钟学习极大似然估计
https://endlesslethe.com/easy-to-learn-mle.html

极大似然估计其实是理想地认为，对于极少的样本观测，我们观测到的样本很可能就是发生概率最大的。

Latex数学公式简明教程
https://endlesslethe.com/latex-math-formula-tutorial.html

最小二乘法是勒让德( A. M. Legendre)于1805年在其著作《计算慧星轨道的新方法》中提出的。它的主要思想就是求解未知参数，使得理论值与观测值之差（即误差，或者说残差）的平方和达到最小：

把  矩阵的行列互换之后得到的矩阵，称为  的转置矩阵，记作 A^T
一个n阶方阵A称为可逆的，或非奇异的，如果存在一个n阶方阵B，使得AB=BA=E则称B是A的一个逆矩阵。A的逆矩阵记作A-1。


3D矩阵变换中，投影矩阵是最复杂的。位移和缩放变换一目了然，旋转变换只要基本的三角函数就能想象出来，投影矩阵则很难凭借直觉想象出来。

当样本量m很少，小于特征数n的时候，这时拟合方程是欠定的，需要使用LASSO。当m=n时，用方程组求解。当m>n时，拟合方程是超定的，我们可以使用最小二乘法。

投影矩阵推导(翻译)
https://www.cnblogs.com/davelink/p/5623760.html

损失函数（loss function）或代价函数（cost function）是将随机事件或其有关随机变量的取值映射为非负实数以表示该随机事件的“风险”或“损失”的函数。在应用中，损失函数通常作为学习准则与优化问题相联系，即通过最小化损失函数求解和评估模型。

机器学习：Python中如何使用最小二乘法
https://www.cnblogs.com/lc1217/p/6514734.html

机器学习:形如抛物线的散点图在python和R中的非线性回归拟合方法
http://www.cnblogs.com/lc1217/p/6519860.html


机器学习：Python实现单层Rosenblatt感知器
https://www.cnblogs.com/lc1217/p/6530177.html

Rosenblatt感知器详解
https://www.cnblogs.com/lanix/p/5003521.html

Python 机器学习
https://www.cnblogs.com/lc1217/category/960537.html

深度学习：Keras入门(一)之基础篇
https://www.cnblogs.com/lc1217/p/7132364.html

常见硬盘IOPS参考值
https://elf8848.iteye.com/blog/1731301

对机械硬盘和SSD固态硬盘IOPS、吞吐量的压测对比
http://blog.itpub.net/28916011/viewspace-2200027/

硬盘IOPS与读写速度
https://blog.csdn.net/star890124/article/details/52004138

磁盘性能指标--IOPS、吞吐量及测试
https://blog.51cto.com/wushank/1708168

centos7 df 命令卡死
https://www.cnblogs.com/John-2011/p/9577038.html

systemctl restart proc-sys-fs-binfmt_misc.automount;

调用谷歌翻译API
https://www.jianshu.com/p/6187d5915f70

解决pip的警告
pip install pyopenssl ndg-httpsclient pyasn1



禁用 root ssh，增加新用户

useradd wawa
passwd wawa
usermod -G wheel wawa

vi /etc/ssh/sshd_config
    port 36000
    PermitRootLogin no
    
    
用sklearn做一个完整的机器学习工程——以波士顿房价预测为例。（一、用自定义转换器、Pipeline Feature_Union做特征工程）
https://blog.csdn.net/PythonstartL/article/details/82874932
https://blog.csdn.net/PythonstartL/article/details/82991548
https://blog.csdn.net/PythonstartL/article/details/83347173

https://blog.csdn.net/sdoddyjm68/article/details/78991699

香港大学深度学习课件笔记（1.5）
https://blog.csdn.net/sdoddyjm68/article/details/78409202

总结：sklearn机器学习之特征工程
https://www.jianshu.com/p/1c4ec02dd33f

Sklearn 笔记
https://www.cnblogs.com/yaoz/tag/Sklearn/

机器学习中的范数规则化之（一）L0、L1与L2范数
https://blog.csdn.net/zouxy09/article/details/24971995
笔记︱范数正则化L0、L1、L2-岭回归&Lasso回归（稀疏与特征工程）
https://blog.csdn.net/sinat_26917383/article/details/52092040

机器学习中的损失函数 （着重比较：hinge loss vs softmax loss）
https://blog.csdn.net/u010976453/article/details/78488279

zouxy09博客原创性博文导航：怀着对机器学习和计算机视觉
https://blog.csdn.net/zouxy09/article/details/14222605

Python机器学习库scikit-learn实践
https://blog.csdn.net/zouxy09/article/details/48903179    


iris-经典案例解析-机器学习
https://www.jianshu.com/p/da18f0cd7f60

机器学习训练数据
http://archive.ics.uci.edu/ml/index.php

tensorflow提示未编译使用SSE4.1，SSE4.2等问题的解决方法
https://blog.csdn.net/qq_36511757/article/details/77895316


Ubuntu 18.04 安装 nodejs
Ubuntu 18.04 LTS Server npm : Depends: node-gyp (>= 0.10.9) but it is not going to be installed [duplicate]
https://askubuntu.com/questions/1057737/ubuntu-18-04-lts-server-npm-depends-node-gyp-0-10-9-but-it-is-not-going

ubuntu无法修正错误，因为您要求某些软件包保持现状...解决办法
https://blog.csdn.net/buppt/article/details/78914234

sudo apt install npm

    npm : 依赖: node-gyp (>= 0.10.9) 但是它将不会被安装
    
sudo apt install node-gyp

    node-gyp : 依赖: nodejs-dev 但是它将不会被安装    
    
sudo apt install nodejs-dev

    nodejs-dev : 依赖: libssl1.0-dev (>= 1.0.2) 但是它将不会被安装    
    
sudo apt install libssl1.0-dev    
sudo apt -f install npm


How to install Node.js and npm on Ubuntu 18.04
https://linuxize.com/post/how-to-install-node-js-on-ubuntu-18.04/


## 小型团队工程化 CheckList

git 不显示中文
git config --global core.quotepath false

tar 压缩中文文件乱码
sudo apt install p7zip-full
7za a x.7z *.ipynb *.py


Issue in installing php7.2-mcrypt
https://stackoverflow.com/questions/48275494/issue-in-installing-php7-2-mcrypt
https://lukasmestan.com/install-mcrypt-extension-in-php7-2/


apt install php-pear
pecl version

apt-get -y install gcc make autoconf libc-dev pkg-config
apt-get -y install php7.2-dev libmcrypt-dev
pecl install mcrypt-1.0.1

bash -c "echo extension=/usr/lib/php/20170718/mcrypt.so > /etc/php/7.2/cli/conf.d/mcrypt.ini"
php -i | grep "mcrypt"

Encrypt/decrypt with XOR in PHP
https://stackoverflow.com/questions/14673551/encrypt-decrypt-with-xor-in-php


2018-04-27 《程序员的职业素养 - The Clean Coder》
https://blog.csdn.net/sunzhongyuan888/article/details/80396825

 好程序员与坏程序员的差别详细分析！
http://www.sohu.com/a/223781695_413876
 
 什么样的人当不好程序员？
 https://36kr.com/p/5042433.html
 
 一个十几年程序员给所有新老程序员的忠告
 https://www.jianshu.com/p/57fd54974d71
 
 好的程序员和差的程序员
 https://blog.csdn.net/dutao53486944/article/details/20009039
 
 金牌员工下班前必做的6件事
 https://jingyan.baidu.com/article/bad08e1ea2e3a709c9512168.html
 
 
 # 格式化大硬盘，大于 4 G

    # 查看硬盘数
    fdisk -l
    
    # 用 parted 进行大分区
    parted /dev/vdb
        mklable gpt
        print
        mkpart primary 0 4295GB
        gpt
        
    # 查看分区结果
    fdisk -l
    
    # 格式化
    mkfs.ext4 -T largefile /dev/vdb1
    
    # 挂载
    mount -t ext4 /dev/vdb1 /data2
    
    # 设置重启后也生效
    echo '/dev/vdb1   /data2  ext4    defaults    0   0'  >>/etc/fstab
    
ganglia 不显示堆叠图
Missing stacked graphs on new ganglia-web 3.5.3 install
https://sourceforge.net/p/ganglia/mailman/ganglia-general/thread/alpine.DEB.2.02.1209191232500.4417@vukovar/
rm /var/lib/ganglia-web/conf/ganglia_metrics.cache    

Python Encrypting with PyCrypto AES
https://stackoverflow.com/questions/14179784/python-encrypting-with-pycrypto-aes

推荐 ：一文读懂最大似然估计(附R代码)
http://www.ijiandao.com/2b/baijia/171559.html

数据科学家应知必会的6种常见概率分布
https://blog.csdn.net/kicilove/article/details/78655856

通过阿里云API(php)搭建秒级DDNS动态域名解析
https://www.zimrilink.com/share/aliddns.html




代码的好味道和坏味道之22种坏味道
https://blog.csdn.net/zxh19800626/article/details/84781597

谈谈我们公司如何做Code Review
https://blog.csdn.net/zxh19800626/article/details/84995166#comments


office 文件预览
https://products.office.com/zh-cn/office-online/documents-spreadsheets-presentations-office-online?rtc=1
https://products.office.com/en-us/office-online/documents-spreadsheets-presentations-office-online?rtc=1
libreoffice


ssh2,node-rdp,xterm,monaco-editor,socket.io

请问感冒的分类有哪几种?
http://www.bu-shen.com/shen-usnyhbbn.htm

Web code editor with Monaco code editor, JQuery file tree browser , nodejs
https://github.com/moorthi07/marscode

Add close button to jquery ui tabs?
https://stackoverflow.com/questions/14357614/add-close-button-to-jquery-ui-tabs
http://jqueryui.com/tabs/#manipulation

How can I get file extensions with JavaScript?
https://stackoverflow.com/questions/190852/how-can-i-get-file-extensions-with-javascript

Linux中profile、bashrc、bash_profile之间的区别和联系
https://blog.csdn.net/m0_37739193/article/details/72638074

linux中CentOS、Ubuntu、Debian三个版本系统 差别
https://www.cnblogs.com/baichuanhuihai/p/8056976.html

代码规范 : 表驱动法(if switch 真讨厌)
https://blog.csdn.net/qq_22555107/article/details/78884261

umeditor储存型xss漏洞 
https://www.yuag.org/2017/09/19/ueditor%E5%82%A8%E5%AD%98%E5%9E%8Bxss%E6%BC%8F%E6%B4%9E/  

根据白名单过滤 HTML(防止 XSS 攻击)
https://github.com/leizongmin/js-xss/blob/master/README.zh.md


jQuery的.bind() .live() .delegate()和.on()之间的区别
https://blog.csdn.net/weixin_38840741/article/details/80272203

Connecting to remote SSH server (via Node.js/html5 console)
https://stackoverflow.com/questions/38689707/connecting-to-remote-ssh-server-via-node-js-html5-console