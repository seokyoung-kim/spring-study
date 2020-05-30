## Annotation으로 설정할 때의 장점
### XML로 설정할 때의 모듈 변경 방법

결합 상태를 바꾸기 위한 코드가 나중에 수정될수도 있기 때문에 코드가 수정되지 않고 둘의 결합 상태를 바꾸기 위해 XML로 설정했었음.

> 객체를 바꾸면 설정도 자동으로 바꿀수는 없을까?
아예 코드에 메타 데이터를 심어버리는 것으로 해결

@Component를 발견하면 이것을 객체화함.

객체를 바꾸면 설정이 자동으로 바뀌기 때문에 이것이 Annotation의 장점

### DI 지원을 위한 스프링 어노테이션
#### Autowired 어노테이션
**Autowired**란 Dependency를 Injection해주는 Annotation으로 xml의 역할을 대신함.
Autowired를 붙이면 DI를 하는 property를 지울수 있음.
setter 메소드에 Autowired를 붙이면 됨.

특별하게 지시하지 않으면 객체를 생성할 떄 클래스 안에 가서 Autowired를 뒤져보지 않음. 뒤져보도록 부탁해야 함.

그 키워드를 심어야 함
+ namespace -> context 추가

```
<context:annotation-config />
```
이후 위 키워드를 추가함으로써 annotation을 찾게 함
