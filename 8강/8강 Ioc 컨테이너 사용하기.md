## Application Context
> DI 지시서를 읽고 생성하고 조립해주는 객체

+ ApplicationContext는 인터페이스명
```
ApplicationContext context = new ClassPathXmlApplicationContext("config.xml");
```

### ApplicationContext 종류
+ ClassPathXmlApplicationContext : 루트로 지정하고 싶을 때 사용
+ FileSystemXmlApplicationContext : 파일시스템의 경로로 지정할 때 사용
+ XmlWebApplicationContext : 웹의 URL로 지정할 때 사용
+ AnnotationConfigApplicationContext : 어노테이션을 활용하여 스캔할 때 사용

### 조립순서
1. ApplicationContext 인터페이스로 객체를 생성.

2. 자바 프로젝트를 Maven 프로젝트로 변환
> 1. project명 오른쪽 마우스
> 2. configure
> 3. Convert to Maven Project 
> 4. pom.xml 파일 자동 생성
> 5. Dependencies로 진입하여 add 버튼 클릭
> 6. Enter groupid에 springframework 검색
> 7. spring-context 선택

3. context는 bean들이 객체화되어 있는것을 담는 IoC Container가 됨

4. context.getBean 형태로 객체들을 꺼내게 되는데 이는 object 형태로 나오기 때문에 형변환이 이루어져야 함

5. 위 방법이 아니면 getBean 안에 인자를 ExamConsole 인터페이스를 구현하는 클래스들로 꺼내어 형변환을 피할수도 있음
```
ExamConsole console = context.getBean(ExamConsole.class);
```