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