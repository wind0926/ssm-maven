# ssm-maven
smm框架+maven+oracle的旅游后台系统
该项目是maven工程搭建，以及基于oracle数据库的商品表信息，并完成SSM整合. 

数据库Oracle，Oracle数据表存放在表空间下，每个用户有自己的独立的表空间，共有8张表：产品表、订单表、会员表、旅客表、用户表、角色表、资源权限表、日志表

<h3>ssm界面运用AdminLTE框架</h3>

<h3>创建maven工程</h3>  
1.project父工程

2.创建子模块  
3.在pom.xml导入依赖  
4.编写实体类  
5.编写业务接口  
6.编写持久层接口  



<h3>功能介绍：</h3>  

<h4>1.商品查询</h4> 
    一、Spring环境搭建 
    
      1.编写Spring配置文件applicationContent.xml  
      
      2.使用注解配置业务层  
      
    二、SpringMVC环境搭建
    
      1.web.xml配置springmvc核心控制器
      
      2.springmvc配置文件springmvc.xml
     
     三、spring与Spring MVC 整合在web。xml中配置
     
     四、Spring与mybatis整合
     
      1.把myatis配置文件（mybatis.xml）中内容配置到Spring配置文件中，mybatis中内容清除。
      
      2.Spring接管mybatis的session工厂
      
      3.自动扫描所有mapper接口和文件
      
      4.配置Spring事务
      
![image](https://github.com/wind0926/ssm-maven/blob/master/images/%E6%8D%95%E8%8E%B7.PNG)

<h4>2.商品添加</h4>
    1.商品添加页面product.jsp
    
    2.在Controller中编写方法
    
    3.在Dao中编写方法
  
<h4>3.订单查询</h4> 
    
    1.创建订单表（与产品表有关productID,与memberID表有关会员表）
    
    2.创建orader实体类
    
    3.创建会员表（订单与会员多对一公园西，在订单中创建外键关联）
    
    4.创建member实体类
    
    5.创建旅客表travellr
    
    6.创建traveller实体类
    
    7.创建中间表（order_traveller）旅客表与订单之间多对多关系
    
    8.编写订单查询页order-list.jsp
    
    9.编写Contorller
    
    10.编写dao，IorderDao和IProductDao的findById
    
![image](https://github.com/wind0926/ssm-maven/blob/master/images/%E6%8D%95%E8%8E%B71.PNG)    

<h4>4.订单分页查询</h4> 
    
    运用PageHelper分页插件，是mybatis工具
    
    1.引入jar包，在pom.xml中添加依赖
    
    2.在mybatis配置xml中配置拦截器插件
    
    3.在Spring配置文件中配置拦截器
    
    4.编写service
    
    5.编写Controller
    
    6.编写订单分页查询页
    
    
<h4>5.订单详情查询</h4> 
  
    1.编写order-show.jsp
    
    2.编写Controller
    
    3.编写Dao
    
<h4>6.用户管理 </h4> 
    
    SSM权限操作
    
      spring Security框架为Spring项目组中提供安全认证与授权

      1.导入依赖
      
      2.web.xml文件中创建spring Security filterChain
      
      3.Spring Security.xml核心配置文件配置
      
      Spring security使用数据库认证
      
       userDetails:封装当前进行认证的用户信息，接口
       
       userdetailsService:用来规范认证方法
      
![image](https://github.com/wind0926/ssm-maven/blob/master/images/%E6%8D%95%E8%8E%B72.PNG)     

<h4>7.角色管理</h4> 

![image](https://github.com/wind0926/ssm-maven/blob/master/images/%E6%8D%95%E8%8E%B73.PNG)
    
<h4>8.资源权限管理</h4> 
<h4>9.权限关联与控制</h4>
    
    1.spring-security中开启JSR-250注解
    
    2.在指定方法使用@RoleAllowed（"ADMIN"），表示当前这个方法只有admin角色才能访问
    
    3.必须在pom.xml找那个导入依赖
    
 ![image](https://github.com/wind0926/ssm-maven/blob/master/images/%E6%8D%95%E8%8E%B74.PNG)   
 
<h4>10.AOP日志处理 </h4> 
  
  创建LogAOP 切面类
  前置通知 @Before
  后置通知 @After
  
 

 
  

  
 
