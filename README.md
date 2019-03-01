# kakao-clone

Kakao Desktop App Clone

## 1. index.html

- 웹 서버들은 index파일을 먼저 찾게 되어 있다.
- html은 수많은 tag로 이루어져 있다.
- !DOCTYPE html
    - CHROME에게 html문서임을 알려준다.
    - self-contained tag이므로 따로 닫아줄 필요가 없다.


## 2. tag
- tag는 어떻게 정의하는가.
```html
<name attribute = "value">Content</name>
<human gender = "male">Human</human>
<dog breed = "german-shepard">Dog</dog>
<title>This is the title of the document</title>
```
- tag는 항상 열고 닫아야 한다
- head
    - 유저가 볼 수 없다.
    - 다만 내 웹사이트의 정보(information)만 제공할 뿐.
- body
    - 여기에 작성하고 싶은 내용(content)이 제공된다.
    - h1부터 h6까지. 오른쪽으로 갈수록 글자 크기가 작아진다.
- meta tag
  - 추가로 제공하는 브라우저를 위한 정보
  - charset은 어떤 방식으로 문서를 encoding할 건지 알려줌
  - 정말 많은 종류의 meta tag가 존재한다.
- semantic tag vs. non-semantic tag
    - semantic은 의미가 있는 tag, non-semantic은 의미가 없는 tag
    - non-semantic tag의 예로 div(의미 없음)와 span(짧은)이 있다.
        - 둘 다 tag들을 담는 container의 역할을 한다.
        - span의 경우 text를 위한(ex.title,p) container이다.
- tag의 name
    - tag가 같은 tag일 경우 구분을 해줘야한다. 뭐가 뭔지 모르기 때문에.
    - id : 고유 이름이므로 공유 불가능  ex. 여권번호
    - class : 동일 속성 공유 가능   ex. 국적, 이름
    - 웹 상에서 고유의 element가 있는 경우는 거의 없기에 class를 주로 사용하게 된다.


## 3. style.css
- css파일은 selector파트와 property파트로 이루어져 있다.
    - selector파트는 {}을 이야기하고, 괄호 안에 무수히 많은 property가 들어갈 수 있다.
    - selector파트에 id(#name)과 class(.name)을 추가할 수 있다.
    - 이를 통해 tag에 속성(attribute)를 부여할 수 있다.
- html과 css를 연결하는 방법
    - inline : html 내부에 css파일을 넣는다.
        - html의 head부분에 style을 넣는다.
        - style은 css를 html파일 상단에 붙이게 하는 걸 가능케 한다.
        - 단점 : 여러 개의 html파일에 적용할 수 없다. 다 복붙해야해. 즉, 비효율적이다.
    - external : css파일을 따로 생성한다.
        - 모든 html문서 head에 연결을 해야 한다.
        - 유지/보수 때 css파일만 수정하면 된다.
- Box Model
    - content, padding, border, margin