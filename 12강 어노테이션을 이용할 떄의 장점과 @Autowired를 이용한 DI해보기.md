## Annotation으로 설정할 때의 장점
### XML로 설정할 때의 모듈 변경 방법

결합 상태를 바꾸기 위한 코드가 나중에 수정될수도 있기 때문에, 코드가 수정되지 않고 둘의 결합 상태를 바꾸기 위해 XML로 설정하였다.

```그렇다면 객체를 변경 시 설정도 자동으로 바꿀수는 없을까?```

> 아예 코드에 메타 데이터를 심어버리는 것으로 해결

@Component를 발견하면 스프링은 이것을 객체화한다.

객체를 바꾸면 설정이 자동으로 바뀌기 때문에 이것이 **Annotation을 사용할 때의 장점**이다.

### DI 지원을 위한 스프링 어노테이션
#### Autowired 어노테이션
**Autowired**란 Dependency를 Injection해주는 Annotation으로 xml의 역할을 대신하는 어노테이션이다.

Autowired를 붙이면 DI를 하는 property를 지울수 있다. 이후 setter 메소드 위에 Autowired를 붙이면 된다.

특별하게 지시하지 않으면 객체를 생성할 떄 클래스 안에 가서 Autowired를 찾아보지 않으므로 이를 스프링에 부탁하여야 한다.

키워드를 추가하기 위해 context namespace를 이용한다.
1. setting.xml의 namespace -> context 추가
2. 이후 setting.xml 코드 안에 아래 코드를 추가한다.

```
<context:annotation-config />
```
이후 위 키워드를 추가함으로써 annotation을 찾게 한다.

> 그렇다면 ref나 value와 같은 키워드가 없는 Autowired 어노테이션은, 무엇을 근거로 바인딩을 해줄것인가?
