# JPA
	JPA는 인터페이스로서 자바 표준명세서   
	인터페이스를 사용하기 위해서는 Hibernate, Eclipse Linkk 와 같은 구현체가 필요하다   
	구현체를 더 쉽게 사용하고자 Spring Data JPA라는 모듈을 통해 JPA를 이용한다   
   
JPA <- Hibernate <- Spring Data JPA   
   
```java
@Id
@GeneratedValue(strategy = GenerationType.IDENTITY)
private Long id;
```
