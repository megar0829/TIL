# 마크다운 (markdown)

- ### 마크다운이란
   다양한 환경에서 사용되는 텍스트 형식으로 문법을 어떻게 사용하느냐에 따라서 문서의 형태가 달라진다.


>### 마크다운 문법
1. 제목(Heading)
  - #의 개수에 따라 크기의 조절이 가능하며 h1~h6 까지 표현 가능
  - ex) # h1,  ## h2, ~~ ####### h6
  - ` 반드시 띄어쓰기를 해야만 한다.`
    - # h1
    - ## h2
    - ### h3
    - #### h4
    - ##### h5
    - ###### h6
2. 목록 (List)
  - 순서가 있는 리스트(ol)와 순서가 없는 리스트(ul)로 구성
  - 순서가 있는 리스트(ol)
  ```bash
    1. 
    2. 
    3.
  ``` 
  - 순서가 없는 리스트 (ul)
  ```bash
    - 
    - 
    * 
    *   
  ```
  - ` tap , shift + tap 으로 들여쓰기를 조절하며 입력` 
3. 코드블록 (Fenced Code block)
  - 코드블록은 ``` 으로 작성
  - 특정 언어를 명시하면 Syntax Highlighting 적용 가능
  ```{ 
    "firstName" : "Bae",
    "lastName" : "Jeongsik"
   }
   ```

  ```json
  {
    "firstName" : "Bae",
    "lastName" : "Jeongsik"
  }
  ```

  ``` python
  {
    "firstName" : "Bae",
    "lastName" : "Jeongsik"
  }
  ```
  ``` html
  {
   "firstName" : "Bae",
    "lastName" : "Jeongsik"
  }
  ```
4. 코드블록 (Inline Code block)
  - 인라인 코드블록은 `을 사용하여 작성
  ```bash 
  ` 내용 `
  ```
5. 링크 (link)
  - 텍스트를 클릭하여 원하는 링크로 이동
  - [텍스트](해당 URL)
  ```bash
    [구글](https://www.google.com)
  ```
6. 사진 (Image)
  - 원하는 사진을 저장 후 사용
  - 다른 위치에 있을 경우 / 을 사용하여 폴더를 지정
  ```html
  - ![대체텍스트](사진파일명)
  - ![대체텍스트](폴더위치/사진파일명)
  ```

7. 글씨체
  - 진하게 (bold) : **진하게**
  - 기울임 : *기울임*
  - 취소선 : ~~취소선~~
  - 분리선 : ---