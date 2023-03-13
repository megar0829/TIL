># HTML 

WWW (World Wide Web)
: 인터넷으로 연결된 컴퓨터들이 정보를 공유하는 거대한 정보 공간

Web page = HTML + CSS + Javascript
HTML    : Structure (구조)
CSS     : Styling   (디자인)
Javascript : Behaviour (동작) 

HTML (HyperText Markup Language)
: 웹페이지의 의미와 구조를 정의하는 언어

HTML = Hypertext + Markup Language
Hypertext : 웹 페이지를 다른 페이지로 연결하는 링크
Markup Language : 태그 등을 이용하여 문서나 데이터의 구조를 명시하는 언어

HTML Element
- tag (Opening, Closing)
하나의 요소는 여는 태그와 닫는 태그 그리고 내용으로 구성됨
닫는 태그는 태그 이름 앞에 '/' 가 포함되며 닫는 태그가 없는 태그도 존재

HTML Attributes
- 규칙
요소 이름 다음에 바로 오는 속성은 태그 이름과 속성 사이에 반드시 공백이 있어야 한다.
하나 이상의 속성이 있을 경우에는 속성 사이에 공백으로 구분한다.
구조 : 속성이름="속성 값"

HTML 문서와 구조
<!DOCTYPE html>
- 해당 문서가 html 문서라는 것을 나타냄
<html></html>
- 전체 페이지의 콘텐츠를 포함
<title></title>
- 브라우저 탭 및 즐겨찾기 시 표시되는 제목
<haed></haed>
- HTML 문서에 관련된 설명, 설정 등을 지정 하는 태그
- 사용자에게 보여지지 않음
<body></body>
- 페이지에 표시되는 모든 콘텐츠

HTML Text structure
- HTML의 텍스트 구조와 의미를 제공
<h1></h1> : 문서의 최상위 제목
Heading & Paragraphs : h1~6, p
Lists : ol, ul, li
Emphasis & Importance : em, strong

CSS (Cascading Style Sheet)
: 웹 페이지의 디자인과 레이아웃을 구성하는 언어
선택자 : 디자인을 하게 될 태그를 입력
선언 : 속성 + 값 으로 나타내며 실제로 적용될 스타일을 입력

CSS 적용 방법
1. 인라인(Inline) 스타일
- 태그안에 style 속성으로 입력
2. 내부(Internal) 스타일 시트
- head 태그 안에 style 태그를 열어서 입력
3. 외부(Extenal) 스타일 시트
- 별도의 CSS 파일 생성 후 link 태그를 이용해서 불러오기

CSS Selectors
종류
- 기본 선택자
    - 전체 선택자 : *
    - 요소 선택자 : tag
        - 지정한 모든 태그 선택
    - 클래스 선택자 : class
        - 주어진 클래스 속성을 가진 모든 요소를 선택
    - 아이디 선택자 : id
        - 주어진 아이디 속성을 가진 요소를 선택
        - 의미를 나눠야 하기 때문에 아이디를 가진 요소가 하나만 있어야 함
    - 속성 선택자 : attr
- 결합자 (Combinators)
    - 자손 결합자
        - 첫 번째 요소의 자손 선택자들을 모두 선택
    - 자식 결합자
        - 첫 번째 요소의 직계 자식만 선택

Cascade & Specificity
Cascade (계단식)
- 동일한 우선순위를 같는 규칙이 적용될때 CSS에서 마지막으로 나오는 규칙이 적용        
Specificity (우선순위)
- 선택자 별로 정해진 우선순위 점수에 따라 점수가 높은 규칙이 적용
우선순위가 높은 순
1. Importance (사용하지 않음)
    - !important (우선순위를 무시)
2. 우선 순위
    - 인라인 스타일 > id 선택자 > class 선택자 > 요소 선택자
3. 소스 코드 순서
상속
- 기본적으로 CSS는 상속을 통해 부모 요소의 속성을 자식에게 상속함
- 이를 이용해 코드의 재사용성을 높임
- 상속되는 속성 : Text 관련요소, opacity, visibility
- 상속되지 않는 속성 : Box model, position

HTML 관련 사항
- HTML 요소 이름은 대소문자를 구분하지 않지만 "소문자" 사용을 권장
- 큰따옴표를 권장
- 에러가 발생하지 않기 때문에 작성 시 주의
- CSS 인라인 스타일은 사용하지 말 것
: 문서의 유지보수가 힘들어짐, 코드를 이해하기 어려움
- 속성은 되도록 class만 사용하도록 함
: 우선순위 규칙을 신경쓰지 않고 사용할 수 있고 유지보수가 더 쉬워짐
: 문서에서 단 한번 유일하게 적용될 스타일인 경우에만 id선택자 사용을 고려
- CSS 상속 여부는 MDN 문서에서 확인