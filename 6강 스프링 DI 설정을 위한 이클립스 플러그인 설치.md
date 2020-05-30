## 스프링 DI 설정을 위한 이클립스 플러그인 설치
주문서를 XML 형태로 넘겨주어야 하는데 이를 스프링이 이해할 수 있는 지시서 형식대로 넘겨줘야 함. 

설정 파일을 일일히 입력하기 귀찮기 때문에 추가하기 위해 플러그인을 설치

### Eclipse 플러그인 설치 순서
Help -> Eclipse Marketplace -> spring으로 검색 -> Spring Tools 3 설치 -> restart now -> new -> other -> spring -> spring bean configuration file로 생성
```
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
	xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsd">


</beans>
```
> xml 파일로 설정 파일이 만들어짐