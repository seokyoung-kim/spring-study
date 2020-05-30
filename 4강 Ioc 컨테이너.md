# IoC 컨테이너
Dependency들이 담겨서 조립되는 생성되는 컨테이너를 IoC 컨테이너라 한다.

Dependency(부품)을 XML(주문서)에 입력하여 스프링에 제공

컴퓨터는 XML이나 Annotation을 활용.

IoC 컨테이너 안에 작은 부품도 만들기 시작하여 큰 부품 순으로 조립.

## DI 순서
### 일체형
A -> B -> C -> D 의 순서

### 조립형
D -> C -> B -> A의 순서(역순)       
=>Inversion of Control(역순으로 객체를 생성)

> 결국 Dependency들을 담는 Container지만 조립되고 결합까지 되며, 결합 순서가 역순이기 때문에 IoC Container라 지칭한다.