#spring security  

  1.简介  
    Spring Security是一个能够为基于Spring的企业应用系统提供声明式的安全访问控制解决方案的安全框架。
  2.springboot下使用 spring security
    ①.创建一个类  WebSecurityConfig继承WebSecurityConfigurerAdapter,并且加上@EnbleWebSercurity注解  
    
 ```java @EnableWebSecurity
     public class WebSecurityConfig extends WebSecurityConfigurerAdapter {}   
```
  
  
  
