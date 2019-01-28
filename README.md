# kakao-clone

Kakao Desktop App Clone

## 2019년 01월 28일

1. index.html 생성

- 웹 서버들은 index파일을 먼저 찾게 되어 있다.
- html은 수많은 tag로 이루어져 있다.
- tag는 어떻게 정의하는가.

2. index.html 수정

- <!DOCTYPE html>
  - CHROME에게 html문서임을 알려준다.
  - self-contained tag이므로 따로 닫아줄 필요가 없다.
- tag는 항상 열고 닫아야 한다
- <head></head>
    - 유저가 볼 수 없다.
    - 다만 내 웹사이트의 정보(information)만 제공할 뿐.
- <body></body>
    - 여기에 작성하고 싶은 내용(content)이 제공된다.
    - h1부터 h6까지. 오른쪽으로 갈수록 글자 크기가 작아진다.
- meta tag
  - 추가로 제공하는 브라우저를 위한 정보
  - charset은 어떤 방식으로 문서를 encoding할 건지 알려줌
  - 정말 많은 종류의 meta tag가 존재한다.
