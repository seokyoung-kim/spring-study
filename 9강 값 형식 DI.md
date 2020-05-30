## 값 형식의 속성에 값 설정하기

+ property에 ref가 아닌 value로 설정      
```
	<bean id="exam" class="spring.di.entity.NewlecExam">
		<property name="kor" value="10"></property>
	</bean>
```
위와 같이 작성하고 실행하면 오류가 난다.
> NewlecExam 클래스에 kor 변수를 지정할 수 있는 set함수가 없기 때문

+ setter함수와 getter함수를 생성
> 1. 마우스 오른쪽 버튼
> 2. source -> generate getters and setters

+ 중첩 태그로 value태그에 값을 넣을수도 있다.
```
<property>
    <value>10</value>
</property>
```
