---
title: Annotation 정리
categories: [spring]
comments: false
---

<h3>내가 보려고 정리한 어노테이션 모음</h3>
- @Configuration
    
    설정파일로 등록
- @RequiredArgsConstructor
  
    초기화되지 않은 final이나 nonnall 생성자 생성
  
    의존성 주입 시 사용
- DI (Dependency Injection, 의존성 주입)

  - @Autowired
  
    스프링 프레임워크에서 지원
  
    타입->이름 순서로 비교하여 의존성 주입
    
  - @Resource
  
    자바에서 지원
  
    이름->타입 순서로 비교
  - @Inject
  
    자바에서 지원
    
    타입->이름 순서로 비교
  
- 스프링 컨테이너에 Bean 등록
  
  * @Bean
    
    주로 @Configuration 내에서 사용
  
    개발자가 컨트롤 불가능한 외부 라이브러리 등록
  
  * @Component

    개발자가 구현한 클래스 bean으로 등록
  
- 컨트롤러

  * @Controller

    ViewResolver이용하여 View 반환
  
    @ResponseBody 이용하여 HttpMessageConverter가 동작해 데이터 반환도 가능

  * @RestController

    Spring MVC Controller에 @ResponseBody 추가
  
    Json형태로 객체 데이터 반환
  
- Jpa
  
  * @DynamicInsert
  
    jpa insert 시 널값인 컬럼 제외, 지정된 default 값 적용
  
  * @DynamicUpdate
  
    jpa update 시 널값인 컬럼 제외
  
    