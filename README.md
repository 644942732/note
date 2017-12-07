#spring security  
  
   ```java
  1.简介  
    Spring Security是一个能够为基于Spring的企业应用系统提供声明式的安全访问控制解决方案的安全框架.  
    
    
   2.springboot下使用 spring security     
    
    ①.引入spring-security依赖  
        
      <dependency>
		  	<groupId>org.springframework.boot</groupId>
			  <artifactId>spring-boot-starter-security</artifactId>
	  	</dependency>
      
      直接访问项目任何一个路径会弹出一个授权框
      
    ①.此时我们需要创建一个类  WebSecurityConfig继承WebSecurityConfigurerAdapter,并且加上@EnbleWebSercurity注解  
      直接访问项目任何一个路径就会直接访问spring-security提供的默认登录页，此时只要通过授权就会跳转到指定的controller，
      默认的是为"/"

      @EnableWebSecurity
     public class WebSecurityConfig extends WebSecurityConfigurerAdapter {
          
          
     }   

      ③.此时，需要指定一个验证方式，首先创建一个方法configGlobal  ，并且注入一个验证管理器建造器 ，

      @EnableWebSecurity
     public class WebSecurityConfig extends WebSecurityConfigurerAdapter {
      @Autowired
	      public void configGlobal(AuthenticationManagerBuilder auth) throws Exception {
	      	auth.inMemoryAuthentication().withUser("12345").password("12345").roles("12345").and().withUser("54321")
				  .password("54321").roles("54321");

	      }
     }   
 ```
  
  
