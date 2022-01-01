# JPA
	JPA는 인터페이스로서 자바 표준명세서   
	인터페이스를 사용하기 위해서는 Hibernate, Eclipse Linkk 와 같은 구현체가 필요하다   
	구현체를 더 쉽게 사용하고자 Spring Data JPA라는 모듈을 통해 JPA를 이용한다   
   
	JPA <- Hibernate <- Spring Data JPA   

#영속성 컨텍스트
```java
@Transactional
public Long update(Long id, PostsUpdateRequestDto requestDto){
 Posts posts = postsRepository.findById(id).orElseThrow(() -> new IllegalArgumentException("해당 게시글이 없습니다. id=" + id));
 posts.update(requestDto.getTitle(), requestDto.getContent());

 return id;
}

public void update(String title, String content){
 this.title = title;
 this.content = content;
}
```
	@Transaction 안에서 DB에서 데이터를 가져오면 이 데이터는 영속성 컨텍스트가 유지된 상태이다   
	
	
