# 타임리프 소개
##### 타임리프 특징
- 서버 사이드 HTML 렌더링 (SSR)
- 네츄럴 템플릿
- 스프링 통합 지원

##### 순수 HTML을 그대로 유지하면서 뷰 템플릿도 사용할 수 있는 타임리프의 특징을 네츄럴 템플릿

# 텍스트 - text, utext

##### Escape
- HTML 문서는 < , > 같은 특수 문자를 기반으로 정의된다. 따라서 뷰 템플릿으로 HTML 화면을 생성할 때는 출력하는 데이터에 이러한 특수 문자가 있는 것을 주의해서 사용해야 함
- 웹 브라우저: Hello <b>Spring!</b>
- 소스보기: Hello &lt;b&gt;Spring!&lt;/b&gt;

##### HTML 엔티티
- 웹 브라우저는 < 를 HTML 테그의 시작으로 인식한다. 따라서 < 를 테그의 시작이 아니라 문자로 표현할 수 있는 방법 이 필요한데, 이것을 HTML 엔티티라 한다. 그리고 이렇게 HTML에서 사용하는 특수 문자를 HTML 엔티티로 변경하는 것을 이스케이프(escape)라 한다. 

##### Unscape
- 타임리프는 두 기능을 제공
  1. th:text -> th:utext
  2. [[...]] -> [(...)]
 
# 변수 - SpringEL

##### 변수 표현식 : ${...}

# 기본 객체들

##### HTTP 요청 파라미터 접근: param
- 예) ${param.paramData}
##### HTTP 세션 접근: session
- 예) ${session.sessionData}
##### 스프링 빈 접근: @
- 예) ${@helloBean.hello('Spring!')}
     
