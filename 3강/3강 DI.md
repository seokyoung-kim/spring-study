# 스프링 프레임워크 코어기능
종속 객체를 생성 조립해주는 도구

## DI
**Dependency Injection**    
Dependency를 부품이라고 생각한다.       
부품 조립이라고 이해하는 것이 더 빠르다.

## Dependency들을 조립하기
### Composition has a
```
class A
{
    private B b;

    public A() {
        b = new B();
    }
}
```
자기가 직접 부품을 가지게 됨
부품을 바꿔 낄 수 없다.(붙박이형)

### Association has a
```
class A 
{
    private B b;
        
    public A() {
        
    }

    public void setB(B b) {
        this.b = b;
    }
}
```
세팅을 해야만 쓸 수 있는 조립형


### Dependency
부품형이 의존성이 훨씬 낮다. 부품을 갈아끼우기 쉬우므로 업데이트가 쉽다. 기업형에서는 부품형을 선호한다.

#### Composition
```
A a = new A();
```

#### Association
```
B b = new B(); // A입장에서 B는 부품     
A a = new A();

a.setB(b);
```

부품이라는 객체를 다른 말로 Dependency라고 함. 이 Dependency를 꽂는 작업을 Injection이라고 함.

> 장점 : 갈아끼우기 쉬움        
> 단점 : 조립해야만 작동을 함

#### Injection(조립 방법)
1. Setter Injection
```
B b = new B();
A a = new A();

a.setB(b);
```
2. Construction Injection
```
B b = new B();
A a = new A(b);
```

> 이 조립을 해주는 역할을 하는 프레임워크가 바로 **스프링** 이다.