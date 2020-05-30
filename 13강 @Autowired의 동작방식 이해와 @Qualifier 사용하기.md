## 객체 생성과 Autowired
1. property injection을 없애고 setter 메소드의 @Autowired로 역할을 넘겨버림
2. ```<context:annotation-config/>``` 코드를 추가하여 객체를 만들고 객체 안의 어노테이션을 찾게 함

### Auto는 무엇을 기준으로 세팅해줄까?
자료형? 변수명?

> 변수명과는 상관이 없음.
자료형을 기준으로 세팅한다.

> 똑같은 bean이 두 개일 때 error가 발생한다.

> 똑같은 bean이 두 개 이상이어서 객체가 모호할 경우 bean에 id를 변수명으로 입력할 때 가능하다.

> 이름이 같지 않을 경우 바인딩이 되지 않음

```이럴 때 사용하는 것이 @Qualifier이다.```
