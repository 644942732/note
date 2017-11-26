#spirng 
对于spring的ioc和di配置有三种方式
	1.xml文件
	2.spring提供的注解
	3.java-based注解
	
Spring的Java配置方式是通过@Configuration 和@Bean这两个注解实现的：
 	1、@Configuration
	作用于类上，相当于一个xml配置文件；
	2、@Bean作用于方法上，相当于xml配置中的<bean>；
	如：
	  @Configuration
		public class AppConfig{
		 @Bean
		public MyService myService() {
 			return new	MyServiceImpl();
   		 }

	相当于：<beans>	
			<beanid="myService"class="com.acme.services.MyServiceImpl"/>
		</beans>
 
 #spirng boot
一、什么是SpringBoot
　　Spring Boot是Spring社区发布的一个开源项目，旨在帮助开发者快速并且更简单的构建项目。大多数SpringBoot项目只需要很少的配置文件。
二。已知常用注解
（1）@RestController和@Controller指定一个类，作为控制器的注解
（4）@Configuration类级别的注解，一般这个注解，我们用来标识main方法所在的类,完成元数据bean的初始化。
（5）@ComponentScan类级别的注解，自动扫描加载所有的Spring组件包括Bean注入，一般用在main方法所在的类上
（6）@ImportResource类级别注解，当我们必须使用一个xml的配置时，使用@ImportResource和@Configuration来标识这个文件资源的类。
（7）@Autowired注解，一般结合@ComponentScan注解，来自动注入一个Service或Dao级别的Bean
（8）@Component类级别注解，是service和controller的父类，用来标识一个组件，，比如我自定了一个filter，则需要此注解标识之后，Spring Boot才会正确识别，


三、SpringBoot快速搭建

	网址：http://start.spring.io;
四、SpringBoot maven 构建项目
	spring-boot-starter-parent：是一个特殊Start，它用来提供相关的Maven依赖项，使用它之后，常用的包依赖可以省去version标签。
1.@SpringBootApplication 是一个综合的注解，目前已知的功能包括@ComponentScan 和@Configuration，它会默认扫描本包及子包的注解。
2.从文档可看出spring boot是支持bean的延迟加载和配置加载顺序的，但是在自动扫描的情况下@Order并不好使，不知是何缘故。

