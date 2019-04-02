<html>

<!Doctype html><html xmlns=http://www.w3.org/1999/xhtml><head>   <meta http-equiv=Content-Type content="text/html;charset=utf-8">

</meta>
</head>

<body>

&nbsp;

<table width="643">
<tbody>
<tr>
<td width="643">

&nbsp;

</td>
</tr>
<tr>
<td width="643">

**&nbsp;**

</td>
</tr>
<tr>
<td width="643">

&nbsp;

</td>
</tr>
</tbody>
</table>

**&nbsp;**

**&nbsp;**

**&nbsp;**

**&nbsp;**

**基于微服务架构模型驱动开发技术**

**&nbsp;**

**&nbsp;**

**&nbsp;**

**&nbsp;**

**&nbsp;**

**&nbsp;**

**&nbsp;**

&nbsp;

<table>
<tbody>
<tr>
<td width="109">

**作者**

</td>
<td width="162">

杨树木

</td>
</tr>
</tbody>
</table>

&nbsp;

&nbsp;

&nbsp;

目录

[1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 引言... 3](https://wordhtml.com/#_Toc5127717)

[2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 技术栈... 4](https://wordhtml.com/#_Toc5127718)

[3&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 开发环境... 4](https://wordhtml.com/#_Toc5127719)

[3.1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 软件需求... 4](https://wordhtml.com/#_Toc5127720)

[3.2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 开发工具... 4](https://wordhtml.com/#_Toc5127721)

[4&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 开发指南... 6](https://wordhtml.com/#_Toc5127722)

[4.1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 开发流程... 6](https://wordhtml.com/#_Toc5127723)

[4.2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 代码骨架... 7](https://wordhtml.com/#_Toc5127724)

[4.3&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 数据建模... 7](https://wordhtml.com/#_Toc5127725)

[4.3.1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Entity的定义... 7](https://wordhtml.com/#_Toc5127726)

[4.3.2&nbsp;&nbsp;&nbsp;&nbsp; Field类型... 8](https://wordhtml.com/#_Toc5127727)

[4.3.3&nbsp;&nbsp;&nbsp;&nbsp; Relationship. 8](https://wordhtml.com/#_Toc5127728)

[4.3.4&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 常量定义... 11](https://wordhtml.com/#_Toc5127729)

[4.3.5&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 全局选项... 11](https://wordhtml.com/#_Toc5127730)

[4.3.6&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 模型示例: demo1.jh. 12](https://wordhtml.com/#_Toc5127731)

[4.4&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 代码生成... 13](https://wordhtml.com/#_Toc5127732)

[4.4.1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 配置代码参数... 13](https://wordhtml.com/#_Toc5127733)

[4.4.2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 自动生成代码... 13](https://wordhtml.com/#_Toc5127734)

[4.5&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 修改配置... 18](https://wordhtml.com/#_Toc5127735)

[4.6&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Maven的构建编绎... 19](https://wordhtml.com/#_Toc5127736)

[4.7&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 单元测试... 21](https://wordhtml.com/#_Toc5127737)

[4.8&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 打包和部署... 22](https://wordhtml.com/#_Toc5127738)

[5&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; FAQ. 23](https://wordhtml.com/#_Toc5127739)

[5.1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 如何构造平台定义result结构... 23](https://wordhtml.com/#_Toc5127740)

[5.2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 返回http错误码... 24](https://wordhtml.com/#_Toc5127741)

[5.3&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 单元测试时报错... 24](https://wordhtml.com/#_Toc5127742)

[5.4&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 数据库连接池启动失败... 25](https://wordhtml.com/#_Toc5127743)

**&nbsp;**

**&nbsp;**

**&nbsp;**

**&nbsp;**

**&nbsp;**

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

# <a name="_Toc5127717"></a>1&nbsp;&nbsp; 引言

基于部门微信服架构+SpringBoot +Jpa+Jhipster模型驱动语言，开发构造基础业务代码骨架系统的快速开发脚手架.

# <a name="_Toc5127718"></a>2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 技术栈

<table width="671">
<thead>
<tr>
<td width="151">

**技术**

</td>
<td>

**类型**

</td>
<td>

**版本**

</td>
<td>

**官网**

</td>
</tr>
<tr>
<td width="151">

ruijie-springframework

</td>
<td>

部门框架

</td>
<td>

2.4

</td>
<td>

[http://gitlab.itnb.cc/](http://start.spring.io/)

</td>
</tr>
</thead>
<tbody>
<tr>
<td width="151">

Spring Boot

</td>
<td>

容器

</td>
<td>

2.1.RELEASE

</td>
<td>

[http://start.spring.io/](http://start.spring.io/)

</td>
</tr>
<tr>
<td width="151">

JPA

</td>
<td>

ORM框架

</td>
<td>

1.3.1

</td>
<td>

[http://start.spring.io/](http://start.spring.io/)

</td>
</tr>
<tr>
<td width="151">

Hibernate

</td>
<td>

ORM框架

</td>
<td>

1.3.1

</td>
<td>

[http://mp.baomidou.com/](http://mp.baomidou.com/)

</td>
</tr>
<tr>
<td width="151">

Maven

</td>
<td>

项目构建管理

</td>
<td>

4.0.0

</td>
<td>

[http://maven.apache.org](http://maven.apache.org/)

</td>
</tr>
<tr>
<td width="151">

Jhipster JDL

</td>
<td>

JDL模型语言

</td>
<td>

5.8.1

</td>
<td>

[https://www.jhipster.tech/](https://www.jhipster.tech/)

</td>
</tr>
</tbody>
</table>

# <a name="_Toc5127719"></a>3&nbsp;&nbsp; 开发环境

## <a name="_Toc5127720"></a>3.1&nbsp;&nbsp;&nbsp; 软件需求

JDK1.8+MySQL5.6+Oracle 10+Maven3.5+

&nbsp;

## <a name="_Toc5127721"></a><a name="_Toc480875847"></a><a name="_Toc467684223"></a>3.2 开发工具

*   安装Eclipse
*   略
*   安装Node
*   略
*   打开命令行，执行以下命令，进行Npm淘宝镜像配置
*   npm config set registry https://registry.npm.taobao.org
*   安装Jhipster
*   npm i -g yarnyarn global add generator-jhipster@5.8.1
*   启动Jhipster
*   在命令行启动 jhipster，确保版本号是5.8.1

# <a name="_Toc5127722"></a>4&nbsp;&nbsp; 开发指南

## <a name="_Toc5127723"></a>4.1 开发流程

&nbsp;

&nbsp;&nbsp;&nbsp; 微服务平台除了引入成熟的技术栈，同时也将目前微服务社区的模型驱动代码生成方案引入到项目中，提高开发效率，降低开发成本，同时减轻开发人员的重复工作。上图中蓝色的部分是可以按照平台开发的指引自动构建完成。

1.  代码骨架：基于Spring Boot的单体服务架构
2.  数据建模：基于JDL语法，模型驱动开发
3.  生成代码：应用建模文件，生成SSH的业务代码
4.  修改配置：针对不同的环境修改配置文件，连接基础服务
5.  CRUD测试：使用Junit单元测试测试所有的接口
6.  业务开发：在上述工作完成的基础上，开发人员可以着手开始业务开发
7.  单元测试：业务开发的同时通过单元测试可以本地完成功能测试
8.  打包部署：平台提供基于maven Jar打包部署方案
9.  对于1-6的步骤，可以通过模型驱动指引快速的得到一个包含所有领域对象CRUD功能、包括单元测试在内的代码。

## <a name="_Toc5127724"></a>4.2 代码骨架

微服务骨架的生成依赖于generator-jhipster，下载骨架地址

部门gitlab: 地址：[http://gitlab.itnb.cc/](http://gitlab.itnb.cc/)

实际项目直接修改将骨架的项目名和包名为实际的项目,可以批量替换骨架的appdemo名称为实际项目名称即可.

## <a name="_Toc5127725"></a>4.3 数据建模

业务建模是骨架开发基础，以下描述一个数据模型建型具体过程相关开发过程.

### <a name="_Toc5127726"></a>4.3.1&nbsp; Entity的定义

entity &lt;entity name&gt; {

&lt;field name&gt; &lt;type&gt; [&lt;validation&gt;*]

}

&nbsp;&nbsp;&nbsp; &lt;entity name&gt;&nbsp; 是指 Entity 的名称

&nbsp;&nbsp;&nbsp; &lt;field name&gt;&nbsp; 是指字段的名称

&nbsp;&nbsp;&nbsp; &lt;type&gt; 是指JHipster支持的字段类型

&nbsp;&nbsp;&nbsp; &lt;validation&gt; 字段的校验规范，可选输入。

*   一个简单的示例

entity D {

lastname String required,

firstname String required,

address String required maxlength(100),

age Integer required min(18)

}

### <a name="_Toc5127727"></a>4.3.2&nbsp;&nbsp;&nbsp;&nbsp; Field类型

Field类型、Java类型、数据库类型的对应关系

<table>
<tbody>
<tr>
<td width="105">

Jhipster类型

</td>
<td width="105">

Java类型

</td>
<td width="102">

CockRoach

数据库类型

</td>
<td width="213">

支持的校验规则

</td>
</tr>
<tr>
<td width="105">

Integer

</td>
<td width="105">

Integer

</td>
<td width="102">

INT

</td>
<td width="213">

required, min, max

</td>
</tr>
<tr>
<td width="105">

Long

</td>
<td width="105">

Long

</td>
<td width="102">

BIGINT

</td>
<td width="213">

required, min, max

</td>
</tr>
<tr>
<td width="105">

BigDecimal

</td>
<td width="105">

BigDecimal

</td>
<td width="102">

DECIMAL(10,2)

</td>
<td width="213">

required, min, max

</td>
</tr>
<tr>
<td width="105">

Float

</td>
<td width="105">

Float

</td>
<td width="102">

REAL

</td>
<td width="213">

required, min, max

</td>
</tr>
<tr>
<td width="105">

Double

</td>
<td width="105">

Double

</td>
<td width="102">

DOUBLE PRECISION

</td>
<td width="213">

required, min, max

</td>
</tr>
<tr>
<td width="105">

Boolean

</td>
<td width="105">

Boolean

</td>
<td width="102">

BOOL

</td>
<td width="213">

required

</td>
</tr>
<tr>
<td width="105">

String

</td>
<td width="105">

String

</td>
<td width="102">

STRING

</td>
<td width="213">

required, minlength, maxlength, pattern

</td>
</tr>
<tr>
<td width="105">

LocalDate

</td>
<td width="105">

LocalDate

</td>
<td width="102">

DATE

</td>
<td width="213">

required

</td>
</tr>
<tr>
<td width="105">

ZonedDateTime

</td>
<td width="105">

ZonedDateTime

</td>
<td width="102">

TIMESTAMP

</td>
<td width="213">

required

</td>
</tr>
<tr>
<td width="105">

Instant

</td>
<td width="105">

Instant

</td>
<td width="102">

TIMESTAMP

</td>
<td width="213">

required

</td>
</tr>
<tr>
<td width="105">

TextBlob

</td>
<td width="105">

String

</td>
<td width="102">

STRING

</td>
<td width="213">

required

</td>
</tr>
</tbody>
</table>

### <a name="_Toc5127728"></a>4.3.3&nbsp;&nbsp;&nbsp;&nbsp; Relationship

*   Relationship的定义格式

relationship (OneToMany | ManyToOne | OneToOne | ManyToMany) {

&lt;from entity&gt;[{&lt;relationship name&gt;[(&lt;display field&gt;)]}] to &lt;to entity&gt;[{&lt;relationship name&gt;[(&lt;display field&gt;)]}]

}

*   可以定义的类型包括 (OneToMany | ManyToOne| OneToOne | ManyToMany)，这些类型和Hibernate中的定义一致。
*   One-to-One (双向关联)

entity Driver

entity Car

relationship OneToOne {

Car{driver} to Driver{car}

}

*   One-to-One (单向关联)

entity Citizen

entity Passport

relationship OneToOne {

Citizen{passport} to Passport

}

*   One-to-Many (双向关联)

entity Owner

entity Car

relationship OneToMany {

Owner{car} to Car{owner}

}

*   One-to-Many (单向关联)

entity Owner

entity Car

relationship ManyToOne {

Car{owner} to Owner

}

*   Many-To-One

entity Owner

entity Car

relationship ManyToOne {

Car{owner} to Owner

}

*   Many-To-Many

entity Driver

entity Car

relationship ManyToMany {

Car{driver} to Driver{car}

}

*   不建议使用ManyToMany，建议使用两个ManyToOne的关联来表达，以保持良好的扩展性
*   &lt;from entity&gt; 是关联的源Entity
*   &lt;to entity&gt; 是关联的目标Entity
*   &lt;relationship name&gt; 是指当前Entity对目标Entity关联关系挂有时命名，
*   &lt;display field&gt; 通常用于定义Entity除了代理主键外的关键标识字段，默认值为ID。这个设置会为DTO增加一个用于友好显示的字段
*   required 表示该关联关系是否必须
*   以下是一个简单的示例，Relationship的关系会应用于生成Liquibase的外键约束，生成符合Hibernate规范的Domain对象关联关系。

entity Book

entity Author {

name String required

}

relationship OneToMany {

Author{book} to Book{writer(name) required}

}

### <a name="_Toc5127729"></a>4.3.4&nbsp;&nbsp;&nbsp;&nbsp; 常量定义

DEFAULT_MIN_LENGTH = 1

DEFAULT_MAX_LENGTH = 42

DEFAULT_MIN_BYTES = 20

DEFAULT_MAX_BYTES = 40

DEFAULT_MIN = 0

DEFAULT_MAX = 41

&nbsp;

entity A {

name String minlength(DEFAULT_MIN_LENGTH) maxlength(DEFAULT_MAX_LENGTH)

content TextBlob minbytes(DEFAULT_MIN_BYTES) maxbytes(DEFAULT_MAX_BYTES)

count Integer min(DEFAULT_MIN) max(DEFAULT_MAX)

}

### <a name="_Toc5127730"></a>4.3.5&nbsp; 全局选项

当前规范约定全局选项统一使用此配置，禁止修改

paginate * with pagination

service * with serviceImpl

dto * with mapstruct

### <a name="_Toc5127731"></a>4.3.6&nbsp; 模型示例: demo1.jh

entity Customer {

firstName String required minlength(1) maxlength(20),

&nbsp;&nbsp; lastName String required minlength(1) maxlength(20),

&nbsp;&nbsp; age Integer required min(0) max(200),

&nbsp;&nbsp; active Boolean required,

&nbsp;&nbsp; emailAddress String required minlength(1) maxlength(100),

&nbsp;&nbsp; dateOfBirth Instant,

&nbsp;&nbsp; country String required minlength(1) maxlength(20),

&nbsp;&nbsp; city String required minlength(1) maxlength(20),

&nbsp;&nbsp; street String required minlength(1) maxlength(200),

}

&nbsp;

entity Product {

&nbsp;&nbsp; code String required minlength(1) maxlength(50),

&nbsp;&nbsp; shortName String required minlength(1) maxlength(50),

&nbsp;&nbsp; longName String required minlength(1) maxlength(200),

&nbsp;&nbsp; description String required minlength(1) maxlength(200)

}

entity CustomerProduct {

&nbsp;&nbsp; amount Integer

}

relationship ManyToOne {

&nbsp;&nbsp; Customer{manager(emailAddress)} to Customer

}

relationship ManyToOne {

&nbsp;&nbsp; CustomerProduct{customer(emailAddress)} to Customer,

&nbsp;&nbsp; CustomerProduct{product(code)} to Product

}

paginate * with pagination

service * with serviceImpl

dto * with mapstruct

## <a name="_Toc5127732"></a>4.4 代码生成

在项目根文件夹（即pom.xml所在的文件夹）,执行如下操作.

### <a name="_Toc5127733"></a>4.4.1&nbsp; 配置代码参数

如果第一次生成，可以修改**.yo-rc.json**代码生成项目包名和项目名。

### <a name="_Toc5127734"></a>4.4.2&nbsp; 自动生成代码

使用命令行 jhipster import-jdl xxx.jh生成代码

一个Entity对应的代码文件包括：

*   src\main\java\cn\com\ruijie\it\demo1\domain\CustomerProduct.java
*   src\main\java\cn\com\ruijie\it\demo1\repository\CustomerProductRepository.java
*   src\main\java\cn\com\ruijie\it\demo1\web\rest\CustomerProductResource.java
*   src\main\java\cn\com\ruijie\it\demo1\service\CustomerProductService.java
*   src\main\java\cn\com\ruijie\it\demo1\service\impl\CustomerProductServiceImpl.java
*   src\main\java\cn\com\ruijie\it\demo1\service\dto\CustomerProductDTO.java
*   src\main\java\cn\com\ruijie\it\demo1\service\mapper\CustomerProductMapper.java
*   src\test\java\cn\com\ruijie\it\demo1\web\rest\CustomerProductResourceIntTest.java

## <a name="_Toc5127735"></a>4.5 修改配置

修改的配置包括 application.properties 和 application-uat.properties，application-pro.properties配置数据库的地址。

log4j2.xml配置日志，默认北京的日志框架配置kafka的话，会同时写入日志到统一服务器。

application.properties配置：

## <a name="_Toc5127736"></a>4.6 Maven的构建编绎

下载的代码骨架，只有包含骨架的源码，因此在执行单元测试或启动项目之前，一定要先进行Maven构建编绎，生成依赖包。

从左侧项目视图，在项目上，使用鼠标右键，选择Run As-&gt;Maven build

第一次会显示，如下界面：

填写说明如下：

Name：Package

Base directory：${selected_resource_loc}

Goals：clean install -DskipTests -Dcheckstyle.skip

点击Apply，然后点击Run，执行打包，打包成功后，可以在项目子目录target找到打包文件

## <a name="_Toc5127737"></a>4.7 单元测试

项目编绎成功后，可以左侧项目视图，右键菜单，执行单元测试： ，在项目上，使用鼠标右键，选择Run As-&gt;JUnit test

## <a name="_Toc5127738"></a>4.8 打包和部署

通过maven管理打包发布。

*   使用命令 mvn clean package 或者使用IDE的菜单，如果要跳过单元测试则加上参数 &ndash;DskipTests
*   和Maven的构建编绎是一样的。都是生成jar包。
*   使用 java -jar appdemo-sevice-1.0-SNAPSHOT.jar 运行部署包
*   如果端口冲突则可以加上参数 --server.port=xxxxx
*   使用浏览器访问
*   [http://localhost:8990/api/my-addresses?page=0&amp;size=20&amp;sort=id,asc](http://localhost:8990/api/my-addresses?page=0&amp;size=20&amp;sort=id,asc)
*   对外rest接口，返回200就是成功。

&nbsp;

# <a name="_Toc5127739"></a>5&nbsp;&nbsp; FAQ

## <a name="_Toc5127740"></a>5.1&nbsp; 如何构造平台定义result结构

**【问题现象】返回如下平台结构**

{ &nbsp;&nbsp;&nbsp;"status":"200", &nbsp;&nbsp;&nbsp;"err":"", &nbsp;&nbsp;&nbsp;data:null }

**【解决方案】**

开发人员只需要在直接在rest返回输出时，定义返回result即可

## <a name="_Toc5127741"></a>5.2&nbsp; 返回http错误码

**【问题现象】**

**返回http状态码**

**【解决方案】**

骨架已集成，http返回错误码，只需要AppCode定义如下：

**public** **static** **final** AppDemoAppCode **_INPUT_NULL_** = **new** AppDemoAppCode(HttpStatus.**_BAD_REQUEST_**, "请求参数为空", "input is null",

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; "001");

&nbsp;

Rest层直接使用：

if (myAddressDTO.getId() == null) {

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; throw AppDemoAppCode.INPUT_NULL.toMsfException();

}

## <a name="_Toc5127742"></a>5.3&nbsp; 单元测试时报错

**【问题现象】**

java.lang.IllegalStateException: Failed to load ApplicationContext

&nbsp;&nbsp;&nbsp; at org.springframework.test.context.cache.DefaultCacheAwareContextLoaderDelegate.loadContext(DefaultCacheAwareContextLoaderDelegate.java:125)

&nbsp;&nbsp;&nbsp; at org.springframework.test.context.support.DefaultTestContext.getApplicationContext(DefaultTestContext.java:108)

&nbsp;&nbsp;&nbsp; at org.springframework.test.context.web.ServletTestExecutionListener.setUpRequestContextIfNecessary(ServletTestExecutionListener.java:190) R)]

&nbsp;

**【解决方案】**

**先maven构造build编绎项目，再执行单元测试。**

## <a name="_Toc5127743"></a>5.4&nbsp; 数据库连接池启动失败

**【问题现象】**

**数据库连接池,依赖北京单点登陆组件,未配置环境变量,则会启动失败**

**【解决方案】**

配置环境变量，env后，再运行，如果还是不生效，有些环境需要重启电脑。

&nbsp;

</body>
</html>
