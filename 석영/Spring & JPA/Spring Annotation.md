![image](https://user-images.githubusercontent.com/96826217/213880735-32ef3dae-eac6-4e28-b156-f40c041bac90.png)

## **🔎 스프링 주요 어노테이션**

-   **@Configuration**: 이 어노테이션을 단 클래스는 빈 설정을 담당하는 클래스가 된다. 이 클래스 안에서 @Bean 어노테이션이 동봉된 메소드를 선언하면, 그 메서드를 통해 스프링 빈을 정의하고 생명주기를 설정하게 된다. 
-   **@ComponentScan**: @Configuration 어노테이션과 함께 쓰면, 이 클래스는 자바 빈 설정 클래스이며, 이 @ComponentScan 어노테이션에서 제공하는 package 속성을 통해 스프링 빈 범위를 정의할 수 있다. 복수개를 지정하고 싶다면 자바 8에서는 단순히 같은 어노테이션을 쓰면 되지만, 자바 7 이하에서는 @ComponentScans 어노테이션 안에 넣으면 된다.
-   **@Import**: @Configuration 어노테이션이 선언된 스프링 설정 클래스를 가져온다. 클래스명을 기입하면 된다. 예를 들면, DB 빈 설정과 DB를 활용하는 빈 (Mybatis 등)을 같이 써야 할 경우 사용하면 된다. 이게 있으면 빈 선언 시 실행 순서도 보장되기 때문에 가끔 튀어나오는 빈 선언 오류도 막을 수 있다.
-   **@Component**: 빈을 선언하는 클래스를 작성하기 위해 넣는 어노테이션이다. 당연히 질리도록 쓸 어노테이션 중 하나일 것이다. 이들은 당연하겠지만 @ComponentScan 의 주요 스캔 대상이다.
-   **@Service**: 사실 @Component 어노테이션과 별 차이가 없어 보인다. 하지만 이 녀석과@Component 어노테이션의 차이점을 알려면 **캡슐화** 개념에 대한 이해가 필요하다. 이 말은 즉슨, 보통 이 어노테이션을 달은 클래스에는 '비즈니스 레이어' 로직에 맞게 짜기 때문에 보통 별도의 데이터를 가지고 있지 않을 것이다. 이건 아주 올바른 사용 케이스이다. 그렇다. 이 어노테이션을 단 클래스는. 그저 업무 메서드만 정의하면 된다. 다른 빈에서 가져와 처리를 하고 결과를 제공하는 그저 비즈니스 로직만 정의하면 된다. 평소처럼. 보통 스프링 MVC에 자주 쓰기 때문에 MVC 소속 어노테이션이라고 생각하지만 MVC 없어도 선언 가능하다.
-   **@Autowired**: 질리도록 쓰는 어노테이션 2번째. 이 어노테이션은 필드, 메서드, 생성자에다가 넣을 수 있다. 아는 그대로다. 스프링 빈을 가져오는 가장 기본적인 방법이다. 해당 클래스에 맞는 빈을 가져오는데, 만약 하나만 있으면 이름 아무렇게나 해도 잘 가져오고, 만약 2개 이상이면 시그니처 명칭에 맞는 빈을 가져오지만, 그 외의 경우는 NoUniqueBeanDefinitionException 예외가 스프링 시작 시 반겨줄 것이다.
-   **@Bean**: @Configuration 선언한 빈 설정 클래스에 빈 선언을 담당하는 어노테이션으로, 메서드에만 넣을 수 있다. 보통은 메소드 이름이 곧 빈 이름으로 탄생한다.
-   **@Lookup**: 이 어노테이션이 선언된 메서드는 리턴 타입을 가진 스프링 빈을 뱉는다. 메소드 본문을 아무리 화려하게 작성해도 씹힌다. 그렇게 작용하도록 AOP 디자인되어 있기 때문이다. 주로 Provider<T> 클래스 감싼 빈 클래스처럼, 싱글톤 빈에 대한 새 인스턴스를 가져오려고 할 때 사용한다. 또 다른 사용법도 있는데 이건 나중에 다루도록 하겠다.
-   **@Primary**: @Configuration 선언한 빈 설정 클래스에 빈 선언을 담당하면서, **기본** 빈 요소를 정의할 때 사용한다. 만약 같은 클래스로 여러 개의 빈을 설정했을 때, 이 어노테이션을 추가로 달면, @Autowired 어노테이션을 통해 빈을 주입 시 이 어노테이션을 가진 빈을 우선적으로 가져온다고 보면 된다. 빈 관리에 편리한 기능이니 여러 빈을 다룰 때 참고하도록.
-   **@Required**: 일반적인 빈 클래스를 초기화 시, 반드시 설정(setter) 해야 하는 setter 메소드를 정의할 때 사용한다. @Bean 선언 및 XML 방식의 빈 선언 시, 만약 이 어노테이션을 통해 빈 속성을 정의하지 않으면 BeanInitializationException 예외가 스프링 시작 시 개발자를 반겨준다. 선언적 어노테이션(@Component 등)에도 넣을 수 있는데, 이 때는 @Autowired(required = false) 어노테이션 주입을 통해서 씹을 수 있다.
-   **@Value**: 생성자, setter 따위의 메서드, 필드 등에다가 스프링에서 설정한 값을 주입할 수 있다. 주로 application.properties 및 스프링이나 자바 property 값을 가져올 때 쓴다.
-   **@DependsOn**: @Bean 및 @Component 등에 정의 및 선언한 빈 생성 시 요구되는 다른 빈을 정의할 때 사용한다. 이 어노테이션을 달면, 이 어노테이션에서 설정한 빈이 등록되지 전까지 어노테이션이 달린 빈을 선언하지 않게 된다. @Import 어노테이션이 클래스 단위 종속성 관리라면, @DependsOn 어노테이션은 빈 단위의 종속성 관리라고 보면 된다.
-   **@Lazy**: 이 어노테이션을 선언한 빈이나 빈 getter 및 필드는 다른 빈처럼 스프링 시작 시 빈 초기화를 하는 것이 아닌, 처음 가져올 때 빈 초기화를 하게 된다, 만약 같은 빈을 가져올 때, 하나라도 이 어노테이션이 달리지 않으면 평소처럼 스프링 시작 시 빈을 초기화하게 되므로, @Bean 및 @Component 어노테이션과 같이 선언하거나, 가져올 때 @Lazy 어노테이션이 다 붙어있는지 확인해야 한다.
-   **@Scope**: 빈의 생명주기를 설정한다. 기본값은 뭐 많이 쓰는 singleton 이고, 그다음 매 가져올 때마다 빈을 생성해서 보내주는 prototype 이 있으며, 스프링 MVC가 있을 경우 요청 단위인 request, 세션 단위인 session 및 globalSession 생명주기를 추가로 설정할 수 있다. 또한 아예 [커스텀 생명주기](https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#beans-factory-scopes-custom-creating) 설정도 가능하다.
-   **@Profile**: 이 어노테이션이 달린 빈은 특정 프로필에서만 동작하도록 설정할 수 있다. 예를 들어 spring.profile=dev 설정 시 @Profile("dev") 일 때만 빈이 초기화된다. 

## **🔎 스프링 부트 주요 어노테이션**

-   **@SpringBootApplication**: 스프링 부트는 기본적으로 이 어노테이션 기준으로 동작하도록 되어 있다. 스프링에서 필수적인 초기화를 담당하는 @EnableAutoConfiguration, @ComponentScan, @Configuration 어노테이션이 함축되어 있다. 이 클래스를 기준으로 빈 스캔을 하게 되며, 여기다가도 @Bean 어노테이션을 이용한 빈 정의도 가능하다.
-   **@EnableAutoConfiguration**: 스프링 부트의 핵심 어노테이션으로, 여태까지 Spring boot 없이 XML이던 자바던 필수적으로 annotation-driven 이나 annotation-config 등... 필수적으로 스프링에 세팅하는 웬만한 것들을 자동 설정하여 **일단 돌아가게** 하도록 도와주는 어노테이션이다.

## **🔎 스프링 MVC 주요 어노테이션**

-   **@Controller**: 이 어노테이션을 통해 웹 요청의 기준을 담당한다. 이 어노테이션을 통해 빈 등록과 동시에 라우팅 테이블에 등록하는 중요한 어노테이션이다.
-   **@ResponseBody**: 컨트롤러 메서드 리턴값에 이 어노테이션을 선언함으로써 스프링은 해당 응답 객체를 클라이언트가 요구하는 요청 내용 유형(Content-Type)에 따라 응답하도록 도와주는 어노테이션이다. 보통은 Jackson 모듈에 의해 json 유형으로 응답해 줄 것이며, 클라이언트가 xml 응답을 요청하면 xml 응답을 해주기도 하고, 경우에 따라 응답 유형을 mimeType 에 따라 설정할 수 있다.(예: MessagePack 등)
-   **@RestController**: 이 어노테이션을 달면, 모든 컨트롤러 메서드는@ResponseBody 어노테이션이 달린 반환 값을 달고 다니게 된다. 주로 REST API 설계 시 필수 어노테이션이라 보면 된다. 물론 ModelAndView 처럼 특수한 유형은 스프링이 평소 그대로 처리하여 응답해 준다.
-   **@RequestMapping(method = RequestMethod.GET, value = "/path")**: 메서드에 달면, 해당 메서드는 이 어노테이션이 설정한 경로를 호출했을 때 메소드가 설정한 응답값을 받게 되며, 컨트롤러 클래스에 달면, 클래스에 설정한 경로를 기준삼아 각 메소드는 클래스 경로의 하위 경로로 추가되어 경로가 잡히게 된다. 또한 method 설정으로 GET만 받거나, POST로 받는 등 특정 HTTP 메서드에만 응답 가능하도록 설정할 수 있으며, GET 의 경우 @GetMapping 같이 메서드 별칭 어노테이션이 있으니 이걸 활용해도 된다. 거기에다가 consumes 속성으로 요청 값에 대한 유형을 한정 지을 수 있으며, produces 속성을 통해 응답 유형을 강제할 수 있다. 이들 둘이 설정 시 지정 타입 안 맞으면400 Bad Request 응답을 뱉도록 스프링에서 설정되어 있다.
-   **@RequestParam(value="name", defaultValue="World")**: 컨트롤러 메서드 인자에서 요청값을 받을 때, 요청 주소(URL)에?뒤로 시작하는 질의 문자열, POST 전송 시 요청받을 키/값, 등을 받을 수 있으며, required 속성으로 필수 여부를 지정할 수 있고, defaultValue 속성을 통해 요청이 없을 경우 대체 기본값을 설정할 수 있다. 만약 required = true 일 경우 해당 파라미터 없이 호출하면 400 Bad Request 응답을 뱉도록 스프링에서 설정되어 있다. **Spring Webflux 사용 시 주의!**: Spring WebFlux 사용시 MVC 패턴을 사용할 수 있으나, @RequestParam 어노테이션은 요청 주소?뒤에 질의 문자열만 받게 된다. 만약 POST 를 통해 얻은 값을 얻고 싶으면, @ModelAttribute 어노테이션을 사용해야 한다. (내 경험 -> [Spring 공식 문서](https://docs.spring.io/spring-framework/docs/current/reference/html/web-reactive.html#webflux-ann-requestparam))
-   **@PathVariable("placeholderName")**: 동적 라우팅 구성 시, (예: /path/to/{placeholderName}) 동적 라우팅에 대한 바인딩 값을 가져오는 인자 어노테이션이다. 길게 설명할 거 없이 동적 라우팅에서 동적 값을 가져올 때 없어서 안될 어노테이션이다.

\*출처 : [https://dev.to/composite/-40c0](https://dev.to/composite/-40c0)
