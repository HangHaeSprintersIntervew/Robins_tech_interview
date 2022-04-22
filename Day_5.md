## 스프린터스 5일차 - JPA, ORM, 스프링 필터
<details>
<summary>스프링 필터랑 인터셉터의 차이점이 무엇인가요?</summary>
<div markdown="1">
- 등록되는 위치가 다르다. (필터는 웹 어플리케이션 컨테이너, 인터셉터는 스프링 컨테이너에서 컨텍스트에 등록된다)
- 호출되는 시점이 다르다. (DispatcherServlet 실행 전에 필터는 호출되며, Interceptor는 그 이후에 호출 된다.)

** 필터
- 필터는 웹 어플리케이션에 등록되어, 전역적으로 처리해야하는 인코딩, 보안 관련된 일을 수행한다.
- 로그인 여부나 권한검사, 오류처리, 인코딩, 웹보안, 요청이나 응답에 대한 로그 등에 사용된다.
** 추가
- 필터의 경우 request, response를 교체 시켜서 제공 가능하나, 
- 인터셉트는 들어온 요청에 대한 ExceptionHandler 등을 통해서 권한을 체크하는데 사용하는 데 적절하다.
</div>
</details>
<details>
<summary>JPA 장점, 단점에 대해 설명해보세요</summary>
<div markdown="1">
- 생산성, 유지보수, 재사용이 가능하다
- 커스텀된 쿼리는 SQL을 직접 작성하는 것이 쉽다.
** 추가
- Query를 직접 작성하지 않아도 되서 생산성이 증가한다
- JPA가 패러다임의 불일치 문제를 해결해주고, 맵퍼나 컨테이너까지 수정해야되는 부분을 처리하기 때문에 유지보수가 쉬워진다.
- 영속성 컨텍스트를 통해 조회된 데이터를 재사용이 가능하다.
</div>
</details>
<details>
<summary>ORM에 대해 설명해보세요</summary>
<div markdown="1">
ORM은 객체와 관계형 데이터 베이스의 데이터를 자동으로 매핑해주는 것입니다. 클래스와 테이블의 불일치를 ORM을 통해 해결합니다.
</div>
</details>
<details>
<summary>생성자 주입 사용시 장점이 무엇이라고 생각하시나요?</summary>
<div markdown="1">
의존성 주입을 누락하는 것을 컴파일 오류를 통해 방지할 수 있고, final 키워드를 통해 값의 불변을 보장할 수 있습니다.<br/>
<br/>
</div>
</details>
<details>
<summary>Entity에 대해 아는대로 설명해보세요</summary>
<div markdown="1">
엔티티는 실체, 객체로 업무에 필요하고 유용한 정보를 저장하고 관리하기 위한 집합으로 볼 수 있습니다.
엔티티에는 자신이 가지고 있는 인스턴스를 설명할 수 있는 속성을 가지게 됩니다.
</div>
</details>
<details>
<summary>Setter를 무분별하게 사용하면 안되는 이유는 무엇인가요?</summary>
<div markdown="1">
- 객체의 일관성을 유지하기 어렵다. 
- 어떠한 의도로 값을 주입하는지 알기 어렵다.
</div>
</details>
