## 설정을 XML에서 Annotation으로 변경
### 지시서 작성방식의 변경
1. xml 파일 내용 제거
2. Java 파일로 변경

##### NewlecAppConfig.java
```
@ComponentScan({배열 형태})
@Configuration
public class NewlecAppConfig {
    @Bean
    public Exam exam() {
        return new NewlecExam();
    }
}
```


### Application Context
#### ApplicationContext 생성하기
```
ApplicationContext context = 
new ApplicationConfigApplicationContext(NewlecAppConfig.class)
```

#### ApplicationContext 종류
+ ClassPathXmlApplicationContext
+ FileSystemXmlApplicationContext
+ XmlWebApplicationContext
+ **AnnotationConfigApplicationContext**

### 클래스 설정 방법
#### 설정 방법 1
```
ApplicationContext context = 
new ApplicationConfigApplicationContext(NewlecAppConfig.class)
```

#### 설정 방법 2
```
ApplicationContext context = 
new ApplicationConfigApplicationContext()
context.register(NewlecAppConfig.class)
context.refresh();
```