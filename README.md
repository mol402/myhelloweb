<html xmlns=http://www.w3.org/1999/xhtml>
<head>   
<meta http-equiv=Content-Type content="text/html;charset=utf-8">

</meta>
</head>

<body>
<p>&nbsp;</p>

<p><strong>&nbsp;</strong></p>
<p><strong>&nbsp;</strong></p>
<p><strong>&nbsp;</strong></p>
<p><strong>&nbsp;</strong></p>
<p><strong>基于微服务架构模型驱动开发技术原型</strong></p>
<p><strong>&nbsp;</strong></p>
<p><strong>&nbsp;</strong></p>
<p><strong>&nbsp;</strong></p>
<p><strong>&nbsp;</strong></p>
<p><strong>&nbsp;</strong></p>
<p><strong>&nbsp;</strong></p>
<p><strong>&nbsp;</strong></p>
<p>&nbsp;</p>
<table>
<tbody>
<tr>
<td width="109">
<p><strong>作者</strong></p>
</td>
<td width="162">
<p>杨树木</p>
</td>
</tr>
</tbody>
</table>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>目录</p>
<p><a href="#_Toc5487044">1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 引言... 3</a></p>
<p><a href="#_Toc5487045">2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 技术栈... 4</a></p>
<p><a href="#_Toc5487046">3&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 开发环境... 4</a></p>
<p><a href="#_Toc5487047">3.1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 软件需求... 4</a></p>
<p><a href="#_Toc5487048">3.2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 开发工具... 5</a></p>
<p><a href="#_Toc5487049">4&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 开发指南... 7</a></p>
<p><a href="#_Toc5487050">4.1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 开发流程... 7</a></p>
<p><a href="#_Toc5487051">4.2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 代码骨架... 8</a></p>
<p><a href="#_Toc5487052">4.3&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 框架已集成的功能... 8</a></p>
<p><a href="#_Toc5487053">4.4&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 数据建模... 9</a></p>
<p><a href="#_Toc5487054">4.4.1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Entity的定义... 9</a></p>
<p><a href="#_Toc5487055">4.4.2&nbsp;&nbsp;&nbsp;&nbsp; Field类型... 9</a></p>
<p><a href="#_Toc5487056">4.4.3&nbsp;&nbsp;&nbsp;&nbsp; Relationship. 10</a></p>
<p><a href="#_Toc5487057">4.4.4&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 常量定义... 12</a></p>
<p><a href="#_Toc5487058">4.4.5&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 全局选项... 13</a></p>
<p><a href="#_Toc5487059">4.4.6&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 模型示例: demo1.jh. 13</a></p>
<p><a href="#_Toc5487060">4.5&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 代码生成... 14</a></p>
<p><a href="#_Toc5487061">4.5.1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 配置代码参数... 15</a></p>
<p><a href="#_Toc5487062">4.5.2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 自动生成代码... 15</a></p>
<p><a href="#_Toc5487063">4.6&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 修改配置... 19</a></p>
<p><a href="#_Toc5487064">4.7&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Maven的构建编绎... 20</a></p>
<p><a href="#_Toc5487065">4.8&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 单元测试... 23</a></p>
<p><a href="#_Toc5487066">4.9&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 打包和部署... 24</a></p>
<p><a href="#_Toc5487067">5&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; FAQ. 25</a></p>
<p><a href="#_Toc5487068">5.1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 如何构造平台定义result结构... 25</a></p>
<p><a href="#_Toc5487069">5.2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 返回http错误码... 26</a></p>
<p><a href="#_Toc5487070">5.3&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 单元测试时报错... 26</a></p>
<p><a href="#_Toc5487071">5.4&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 数据库连接池启动失败... 27</a></p>
<p><strong>&nbsp;</strong></p>
<p><strong>&nbsp;</strong></p>
<p><strong>&nbsp;</strong></p>
<p><strong>&nbsp;</strong></p>
<p><strong>&nbsp;</strong></p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<h1><a name="_Toc5487044"></a>1&nbsp;&nbsp; 引言</h1>
<p>模型驱动开发(MDD Model-Driven Development) :一种新型软件设计方法，面向模型的分析设计方法，系统一开始我们就首先确立实体模型Entity Model，以及它们之间的关系，开发实现表现层、业务服务层和持久层的业务逻辑。</p>
<p>该框架引入模型驱动开发方式，实现基于部门微信服架构+SpringBoot +Jpa+Jhipster模型驱动语言，开发迭代构建基础业务代码骨架系统的模型驱动开发框架原型。.</p>
<h1><a name="_Toc5487045"></a>2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 技术栈</h1>
<table width="671">
<thead>
<tr>
<td width="151">
<p><strong>技术</strong></p>
</td>
<td>
<p><strong>类型</strong></p>
</td>
<td>
<p><strong>版本</strong></p>
</td>
<td>
<p><strong>官网</strong></p>
</td>
</tr>
<tr>
<td width="151">
<p>ruijie-springframework</p>
</td>
<td>
<p>部门框架</p>
</td>
<td>
<p>2.4</p>
</td>
<td>
<p><a href="http://start.spring.io/">http://gitlab.itnb.cc/</a></p>
</td>
</tr>
</thead>
<tbody>
<tr>
<td width="151">
<p>Spring Boot</p>
</td>
<td>
<p>容器</p>
</td>
<td>
<p>2.1.RELEASE</p>
</td>
<td>
<p><a href="http://start.spring.io/">http://start.spring.io/</a></p>
</td>
</tr>
<tr>
<td width="151">
<p>JPA</p>
</td>
<td>
<p>ORM框架</p>
</td>
<td>
<p>1.3.1</p>
</td>
<td>
<p><a href="http://start.spring.io/">http://start.spring.io/</a></p>
</td>
</tr>
<tr>
<td width="151">
<p>Hibernate</p>
</td>
<td>
<p>ORM框架</p>
</td>
<td>
<p>1.3.1</p>
</td>
<td>
<p><a href="http://mp.baomidou.com/">http://mp.baomidou.com/</a></p>
</td>
</tr>
<tr>
<td width="151">
<p>Maven</p>
</td>
<td>
<p>项目构建管理</p>
</td>
<td>
<p>4.0.0</p>
</td>
<td>
<p><a href="http://maven.apache.org/">http://maven.apache.org</a></p>
</td>
</tr>
<tr>
<td width="151">
<p>Jhipster JDL</p>
</td>
<td>
<p>JDL模型语言</p>
</td>
<td>
<p>5.8.1</p>
</td>
<td>
<p><a href="https://www.jhipster.tech/">https://www.jhipster.tech/</a></p>
</td>
</tr>
</tbody>
</table>
<h1><a name="_Toc5487046"></a>3&nbsp;&nbsp; 开发环境</h1>
<h2><a name="_Toc5487047"></a>3.1&nbsp;&nbsp;&nbsp; 软件需求</h2>
<p>JDK1.8+MySQL5.6+Oracle 10+Maven3.5+</p>
<p>&nbsp;</p>
<h2><a name="_Toc5487048"></a><a name="_Toc480875847"></a><a name="_Toc467684223"></a>3.2 开发工具</h2>
<ul>
<li>安装Eclipse</li>
</ul>
<p>略</p>
<ul>
<li>安装Node</li>
</ul>
<p>略</p>
<ul>
<li>打开命令行，执行以下命令，进行Npm淘宝镜像配置</li>
</ul>
<p>npm config set registry https://registry.npm.taobao.org</p>
<ul>
<li>安装Jhipster</li>
</ul>
<p>npm i -g yarnyarn global add generator-jhipster@5.8.1</p>
<ul>
<li>启动Jhipster</li>
</ul>
<p>在命令行启动 jhipster，确保版本号是5.8.1</p>
<h1><a name="_Toc5487049"></a>4&nbsp;&nbsp; 开发指南</h1>
<h2><a name="_Toc5487050"></a>4.1 开发流程</h2>
<p>&nbsp;</p>
<p>&nbsp;&nbsp;&nbsp; 微服务平台除了引入成熟的技术栈，同时也将目前微服务社区的模型驱动代码生成方案引入到项目中，提高开发效率，降低开发成本，同时减轻开发人员的重复工作。上图中蓝色的部分是可以按照平台开发的指引自动构建完成。</p>
<ol>
<li>代码骨架：基于Spring Boot的单体服务架构</li>
<li>数据建模：基于JDL语法，模型驱动开发</li>
<li>生成代码：应用建模文件，生成SSH的业务代码</li>
<li>修改配置：针对不同的环境修改配置文件，连接基础服务</li>
<li>CRUD测试：使用Junit单元测试测试所有的接口</li>
<li>业务开发：在上述工作完成的基础上，开发人员可以着手开始业务开发</li>
<li>单元测试：业务开发的同时通过单元测试可以本地完成功能测试</li>
<li>打包部署：平台提供基于maven Jar打包部署方案</li>
</ol>
<p>对于1-6的步骤，可以通过模型驱动指引快速的得到一个包含所有领域对象CRUD功能、包括单元测试在内的代码。</p>
<h2><a name="_Toc5487051"></a>4.2 代码骨架</h2>
<p>微服务骨架的生成依赖于generator-jhipster，下载骨架地址</p>
<p>部门gitlab: 地址：<a href="http://gitlab.itnb.cc/">http://gitlab.itnb.cc/</a></p>
<p>实际项目直接修改将骨架的项目名和包名为实际的项目,可以批量替换骨架的appdemo名称为实际项目名称即可.</p>
<h2><a name="_Toc5487052"></a><a name="_Toc5301284"></a>4.3 框架已集成的功能</h2>
<p>微服务模型驱动骨架已完成功能集成如下:</p>
<ul>
<li>支持模型JDL建模,自动构造生成业务逻辑代码</li>
<li>支持集成部门功能组件ruijie-springframework,单点登陆验证,微服务网关注册等</li>
<li>支持数据基础操作增删改查询CRUD</li>
<li>支持单元测试CRUD</li>
<li>支持数据业务层标准接口实现定义,数据分层</li>
<li>接口数据DTO封装</li>
<li>支持数据分页查询</li>
<li>支持标准Http状态返回码</li>
<li>支持部门Result结构自己定义返回</li>
</ul>
<h2><a name="_Toc5487053"></a>4.4 数据建模</h2>
<p>业务建模是骨架开发基础，以下描述一个数据模型建型具体过程相关开发过程.</p>
<h3><a name="_Toc5487054"></a>4.4.1&nbsp; Entity的定义</h3>
<p>entity &lt;entity name&gt; {</p>
<p>&nbsp; &lt;field name&gt; &lt;type&gt; [&lt;validation&gt;*]</p>
<p>}</p>
<p>&nbsp;&nbsp;&nbsp; &lt;entity name&gt;&nbsp; 是指 Entity 的名称</p>
<p>&nbsp;&nbsp;&nbsp; &lt;field name&gt;&nbsp; 是指字段的名称</p>
<p>&nbsp;&nbsp;&nbsp; &lt;type&gt; 是指JHipster支持的字段类型</p>
<p>&nbsp;&nbsp;&nbsp; &lt;validation&gt; 字段的校验规范，可选输入。</p>
<ul>
<li>一个简单的示例</li>
</ul>
<p>entity D {</p>
<p>&nbsp; lastname String required,</p>
<p>&nbsp; firstname String required,</p>
<p>&nbsp; address String required maxlength(100),</p>
<p>&nbsp; age Integer required min(18)</p>
<p>}</p>
<h3><a name="_Toc5487055"></a>4.4.2&nbsp;&nbsp;&nbsp;&nbsp; Field类型</h3>
<p>Field类型、Java类型、数据库类型的对应关系</p>
<table>
<tbody>
<tr>
<td width="105">
<p>Jhipster类型</p>
</td>
<td width="105">
<p>Java类型</p>
</td>
<td width="102">
<p>CockRoach</p>
<p>数据库类型</p>
</td>
<td width="213">
<p>支持的校验规则</p>
</td>
</tr>
<tr>
<td width="105">
<p>Integer</p>
</td>
<td width="105">
<p>Integer</p>
</td>
<td width="102">
<p>INT</p>
</td>
<td width="213">
<p>required, min, max</p>
</td>
</tr>
<tr>
<td width="105">
<p>Long</p>
</td>
<td width="105">
<p>Long</p>
</td>
<td width="102">
<p>BIGINT</p>
</td>
<td width="213">
<p>required, min, max</p>
</td>
</tr>
<tr>
<td width="105">
<p>BigDecimal</p>
</td>
<td width="105">
<p>BigDecimal</p>
</td>
<td width="102">
<p>DECIMAL(10,2)</p>
</td>
<td width="213">
<p>required, min, max</p>
</td>
</tr>
<tr>
<td width="105">
<p>Float</p>
</td>
<td width="105">
<p>Float</p>
</td>
<td width="102">
<p>REAL</p>
</td>
<td width="213">
<p>required, min, max</p>
</td>
</tr>
<tr>
<td width="105">
<p>Double</p>
</td>
<td width="105">
<p>Double</p>
</td>
<td width="102">
<p>DOUBLE PRECISION</p>
</td>
<td width="213">
<p>required, min, max</p>
</td>
</tr>
<tr>
<td width="105">
<p>Boolean</p>
</td>
<td width="105">
<p>Boolean</p>
</td>
<td width="102">
<p>BOOL</p>
</td>
<td width="213">
<p>required</p>
</td>
</tr>
<tr>
<td width="105">
<p>String</p>
</td>
<td width="105">
<p>String</p>
</td>
<td width="102">
<p>STRING</p>
</td>
<td width="213">
<p>required, minlength, maxlength, pattern</p>
</td>
</tr>
<tr>
<td width="105">
<p>LocalDate</p>
</td>
<td width="105">
<p>LocalDate</p>
</td>
<td width="102">
<p>DATE</p>
</td>
<td width="213">
<p>required</p>
</td>
</tr>
<tr>
<td width="105">
<p>ZonedDateTime</p>
</td>
<td width="105">
<p>ZonedDateTime</p>
</td>
<td width="102">
<p>TIMESTAMP</p>
</td>
<td width="213">
<p>required</p>
</td>
</tr>
<tr>
<td width="105">
<p>Instant</p>
</td>
<td width="105">
<p>Instant</p>
</td>
<td width="102">
<p>TIMESTAMP</p>
</td>
<td width="213">
<p>required</p>
</td>
</tr>
<tr>
<td width="105">
<p>TextBlob</p>
</td>
<td width="105">
<p>String</p>
</td>
<td width="102">
<p>STRING</p>
</td>
<td width="213">
<p>required</p>
</td>
</tr>
</tbody>
</table>
<h3><a name="_Toc5487056"></a>4.4.3&nbsp;&nbsp;&nbsp;&nbsp; Relationship</h3>
<ul>
<li>Relationship的定义格式</li>
</ul>
<p>relationship (OneToMany | ManyToOne | OneToOne | ManyToMany) {</p>
<p>&nbsp; &lt;from entity&gt;[{&lt;relationship name&gt;[(&lt;display field&gt;)]}] to &lt;to entity&gt;[{&lt;relationship name&gt;[(&lt;display field&gt;)]}]</p>
<p>}</p>
<ul>
<li>可以定义的类型包括 (OneToMany | ManyToOne| OneToOne | ManyToMany)，这些类型和Hibernate中的定义一致。</li>
<li>One-to-One (双向关联)</li>
</ul>
<p>entity Driver</p>
<p>entity Car</p>
<p>relationship OneToOne {</p>
<p>&nbsp; Car{driver} to Driver{car}</p>
<p>}</p>
<ul>
<li>One-to-One (单向关联)</li>
</ul>
<p>entity Citizen</p>
<p>entity Passport</p>
<p>relationship OneToOne {</p>
<p>&nbsp; Citizen{passport} to Passport</p>
<p>}</p>
<ul>
<li>One-to-Many (双向关联)</li>
</ul>
<p>entity Owner</p>
<p>entity Car</p>
<p>relationship OneToMany {</p>
<p>&nbsp; Owner{car} to Car{owner}</p>
<p>}</p>
<ul>
<li>One-to-Many (单向关联)</li>
</ul>
<p>entity Owner</p>
<p>entity Car</p>
<p>relationship ManyToOne {</p>
<p>&nbsp; Car{owner} to Owner</p>
<p>}</p>
<ul>
<li>Many-To-One</li>
</ul>
<p>entity Owner</p>
<p>entity Car</p>
<p>relationship ManyToOne {</p>
<p>&nbsp; Car{owner} to Owner</p>
<p>}</p>
<ul>
<li>Many-To-Many</li>
</ul>
<p>entity Driver</p>
<p>entity Car</p>
<p>relationship ManyToMany {</p>
<p>&nbsp; Car{driver} to Driver{car}</p>
<p>}</p>
<ul>
<li>不建议使用ManyToMany，建议使用两个ManyToOne的关联来表达，以保持良好的扩展性</li>
<li>&lt;from entity&gt; 是关联的源Entity</li>
<li>&lt;to entity&gt; 是关联的目标Entity</li>
<li>&lt;relationship name&gt; 是指当前Entity对目标Entity关联关系挂有时命名，</li>
<li>&lt;display field&gt; 通常用于定义Entity除了代理主键外的关键标识字段，默认值为ID。这个设置会为DTO增加一个用于友好显示的字段</li>
<li>required 表示该关联关系是否必须</li>
<li>以下是一个简单的示例，Relationship的关系会应用于生成Liquibase的外键约束，生成符合Hibernate规范的Domain对象关联关系。</li>
</ul>
<p>entity Book</p>
<p>entity Author {</p>
<p>&nbsp; name String required</p>
<p>}</p>
<p>relationship OneToMany {</p>
<p>&nbsp; Author{book} to Book{writer(name) required}</p>
<p>}</p>
<h3><a name="_Toc5487057"></a>4.4.4&nbsp;&nbsp;&nbsp;&nbsp; 常量定义</h3>
<p>DEFAULT_MIN_LENGTH = 1</p>
<p>DEFAULT_MAX_LENGTH = 42</p>
<p>DEFAULT_MIN_BYTES = 20</p>
<p>DEFAULT_MAX_BYTES = 40</p>
<p>DEFAULT_MIN = 0</p>
<p>DEFAULT_MAX = 41</p>
<p>&nbsp;</p>
<p>entity A {</p>
<p>&nbsp; name String minlength(DEFAULT_MIN_LENGTH) maxlength(DEFAULT_MAX_LENGTH)</p>
<p>&nbsp; content TextBlob minbytes(DEFAULT_MIN_BYTES) maxbytes(DEFAULT_MAX_BYTES)</p>
<p>&nbsp; count Integer min(DEFAULT_MIN) max(DEFAULT_MAX)</p>
<p>}</p>
<h3><a name="_Toc5487058"></a>4.4.5&nbsp; 全局选项</h3>
<p>当前规范约定全局选项统一使用此配置，禁止修改</p>
<p>paginate * with pagination</p>
<p>service * with serviceImpl</p>
<p>dto * with mapstruct</p>
<h3><a name="_Toc5487059"></a>4.4.6&nbsp; 模型示例: demo1.jh</h3>
<p>entity Customer {</p>
<p>firstName String required minlength(1) maxlength(20),</p>
<p>&nbsp;&nbsp;&nbsp; lastName String required minlength(1) maxlength(20),</p>
<p>&nbsp;&nbsp;&nbsp; age Integer required min(0) max(200),</p>
<p>&nbsp;&nbsp;&nbsp; active Boolean required,</p>
<p>&nbsp;&nbsp;&nbsp; emailAddress String required minlength(1) maxlength(100),</p>
<p>&nbsp;&nbsp;&nbsp; dateOfBirth Instant,</p>
<p>&nbsp;&nbsp;&nbsp; country String required minlength(1) maxlength(20),</p>
<p>&nbsp;&nbsp;&nbsp; city String required minlength(1) maxlength(20),</p>
<p>&nbsp;&nbsp;&nbsp; street String required minlength(1) maxlength(200),</p>
<p>}</p>
<p>&nbsp;</p>
<p>entity Product {</p>
<p>&nbsp;&nbsp;&nbsp; code String required minlength(1) maxlength(50),</p>
<p>&nbsp;&nbsp;&nbsp; shortName String required minlength(1) maxlength(50),</p>
<p>&nbsp;&nbsp;&nbsp; longName String required minlength(1) maxlength(200),</p>
<p>&nbsp;&nbsp;&nbsp; description String required minlength(1) maxlength(200)</p>
<p>}</p>
<p>entity CustomerProduct {</p>
<p>&nbsp;&nbsp;&nbsp; amount Integer</p>
<p>}</p>
<p>relationship ManyToOne {</p>
<p>&nbsp;&nbsp;&nbsp; Customer{manager(emailAddress)} to Customer</p>
<p>}</p>
<p>relationship ManyToOne {</p>
<p>&nbsp;&nbsp;&nbsp; CustomerProduct{customer(emailAddress)} to Customer,</p>
<p>&nbsp;&nbsp;&nbsp; CustomerProduct{product(code)} to Product</p>
<p>}</p>
<p>paginate * with pagination</p>
<p>service * with serviceImpl</p>
<p>dto * with mapstruct</p>
<h2><a name="_Toc5487060"></a>4.5 代码生成</h2>
<p>在项目根文件夹（即pom.xml所在的文件夹）,执行如下操作.</p>
<h3><a name="_Toc5487061"></a>4.5.1&nbsp; 配置代码参数</h3>
<p>如果第一次生成，可以修改<strong>.yo-rc.json</strong>代码生成项目包名和项目名。</p>
<h3><a name="_Toc5487062"></a>4.5.2&nbsp; 自动生成代码</h3>
<p>使用命令行 jhipster import-jdl xxx.jh生成代码</p>
<p>一个Entity对应的代码文件包括：</p>
<ul>
<li>src\main\java\cn\com\ruijie\it\demo1\domain\CustomerProduct.java</li>
</ul>
<p>&nbsp;</p>
<ul>
<li>src\main\java\cn\com\ruijie\it\demo1\repository\CustomerProductRepository.java</li>
</ul>
<p>&nbsp;</p>
<ul>
<li>src\main\java\cn\com\ruijie\it\demo1\web\rest\CustomerProductResource.java</li>
</ul>
<p>&nbsp;</p>
<ul>
<li>src\main\java\cn\com\ruijie\it\demo1\service\CustomerProductService.java</li>
</ul>
<p>&nbsp;</p>
<ul>
<li>src\main\java\cn\com\ruijie\it\demo1\service\impl\CustomerProductServiceImpl.java</li>
</ul>
<p>&nbsp;</p>
<ul>
<li>src\main\java\cn\com\ruijie\it\demo1\service\dto\CustomerProductDTO.java</li>
</ul>
<p>&nbsp;</p>
<ul>
<li>src\main\java\cn\com\ruijie\it\demo1\service\mapper\CustomerProductMapper.java</li>
</ul>
<p>&nbsp;</p>
<ul>
<li>src\test\java\cn\com\ruijie\it\demo1\web\rest\CustomerProductResourceIntTest.java</li>
</ul>
<h2><a name="_Toc5487063"></a>4.6 修改配置</h2>
<p>修改的配置包括 application.properties 和 application-uat.properties，application-pro.properties配置数据库的地址。</p>
<p>log4j2.xml配置日志，默认北京的日志框架配置kafka的话，会同时写入日志到统一服务器。</p>
<p>application.properties配置：</p>
<p>&nbsp;</p>
<h2><a name="_Toc5487064"></a>4.7 Maven的构建编绎</h2>
<p>下载的代码骨架，只有包含骨架的源码，因此在执行单元测试或启动项目之前，一定要先进行Maven构建编绎，生成依赖包。</p>
<p>从左侧项目视图，在项目上，使用鼠标右键，选择Run As-&gt;Maven build</p>
<p>第一次会显示，如下界面：</p>
<p>填写说明如下：</p>
<p>Name：Package</p>
<p>Base directory：${selected_resource_loc}</p>
<p>Goals：clean install -DskipTests -Dcheckstyle.skip</p>
<p>点击Apply，然后点击Run，执行打包，打包成功后，可以在项目子目录target找到打包文件</p>
<h2><a name="_Toc5487065"></a>4.8 单元测试</h2>
<p>项目编绎成功后，可以左侧项目视图，右键菜单，执行单元测试： ，在项目上，使用鼠标右键，选择Run As-&gt;JUnit test</p>
<h2><a name="_Toc5487066"></a>4.9 打包和部署</h2>
<p>通过maven管理打包发布。</p>
<ul>
<li>使用命令 mvn clean package 或者使用IDE的菜单，如果要跳过单元测试则加上参数 &ndash;DskipTests</li>
</ul>
<p>和Maven的构建编绎是一样的。都是生成jar包。</p>
<ul>
<li>使用 java -jar appdemo-sevice-1.0-SNAPSHOT.jar 运行部署包</li>
</ul>
<p>如果端口冲突则可以加上参数&nbsp; --server.port=xxxxx</p>
<p>&nbsp;</p>
<ul>
<li>使用浏览器访问</li>
<li><a href="http://localhost:8990/api/my-addresses?page=0&amp;size=20&amp;sort=id,asc">http://localhost:8990/api/my-addresses?page=0&amp;size=20&amp;sort=id,asc</a></li>
</ul>
<p>对外rest接口，返回200就是成功。</p>
<p>&nbsp;</p>
<h1><a name="_Toc5487067"></a>5&nbsp;&nbsp; FAQ</h1>
<h2><a name="_Toc5487068"></a>5.1&nbsp; 如何构造平台定义result结构</h2>
<p><strong>【问题现象】返回如下平台结构</strong></p>
<p>{<br /> &nbsp;&nbsp;&nbsp;"status":"200",<br /> &nbsp;&nbsp;&nbsp;"err":"",<br /> &nbsp;&nbsp;&nbsp;data:null<br /> }</p>
<p><strong>【解决方案】</strong></p>
<p>开发人员只需要在直接在rest返回输出时，定义返回result即可</p>
<h2><a name="_Toc5487069"></a>5.2&nbsp; 返回http错误码</h2>
<p><strong>【问题现象】</strong></p>
<p><strong>返回http状态码</strong></p>
<p><strong>【解决方案】</strong></p>
<p>骨架已集成，http返回错误码，只需要AppCode定义如下：</p>
<p><strong>public</strong> <strong>static</strong> <strong>final</strong> AppDemoAppCode <strong><em>INPUT_NULL</em></strong> = <strong>new</strong> AppDemoAppCode(HttpStatus.<strong><em>BAD_REQUEST</em></strong>, "请求参数为空", "input is null",</p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; "001");</p>
<p>&nbsp;</p>
<p>Rest层直接使用：</p>
<p>&nbsp;if (myAddressDTO.getId() == null) {</p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; throw AppDemoAppCode.INPUT_NULL.toMsfException();</p>
<p>&nbsp;}</p>
<h2><a name="_Toc5487070"></a>5.3&nbsp; 单元测试时报错</h2>
<p><strong>【问题现象】</strong></p>
<p>&nbsp;java.lang.IllegalStateException: Failed to load ApplicationContext</p>
<p>&nbsp;&nbsp;&nbsp; at org.springframework.test.context.cache.DefaultCacheAwareContextLoaderDelegate.loadContext(DefaultCacheAwareContextLoaderDelegate.java:125)</p>
<p>&nbsp;&nbsp;&nbsp; at org.springframework.test.context.support.DefaultTestContext.getApplicationContext(DefaultTestContext.java:108)</p>
<p>&nbsp;&nbsp;&nbsp; at org.springframework.test.context.web.ServletTestExecutionListener.setUpRequestContextIfNecessary(ServletTestExecutionListener.java:190) R)]</p>
<p>&nbsp;</p>
<p><strong>【解决方案】</strong></p>
<p><strong>先maven构造build编绎项目，再执行单元测试。</strong></p>
<h2><a name="_Toc5487071"></a>5.4&nbsp; 数据库连接池启动失败</h2>
<p><strong>【问题现象】</strong></p>
<p><strong>数据库连接池,依赖北京单点登陆组件,未配置环境变量,则会启动失败</strong></p>
<p><strong>【解决方案】</strong></p>
<p>配置环境变量，env后，再运行，如果还是不生效，有些环境需要重启电脑。</p>
<p>&nbsp;</p>

</body>
</html>
