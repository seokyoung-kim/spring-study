## 결합하는 방식
생성자 혹은 set함수

> 결합관계를 바꾸기 위해서는 설정으로 빼서 분리해야 함.

+ java 파일이 아닌 xml 파일로 스프링에게 지시서로 명령
```
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
	xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsd">
	<!-- Exam exam = new NewlecExam(); -->
	<bean id="exam" class="spring.di.entity.NewlecExam" />
	<!-- ExamConsole console = new GridExamConsole(); -->
	<bean id="console" class="spring.di.ui.InlineExamConsole" >
		<!-- console.setExam(exam); -->
		<property name="exam" ref="exam" />
	</bean>
</beans>
```
#### Injection 방법
```<bean>``` 태그에 
id가 같은 이름이 있을 수도 있으므로 class에 패키지명까지 입력
+ 설정을 하기 위해서는 property 명에 set함수를 쓰는데 set을 생략하고 대문자를 소문자로 변경한다.
+ 값은 value 혹은 ref로 들어갈 수 있지만 값 형태가 아니기 때문에 ref로 입력한다.
