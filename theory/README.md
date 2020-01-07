# Kakao Clone Theory

## Module 1. The Tools of a Web Developer

### 1. What Git is
- Git is a version control system.
- In local, we can see all the history of our files in our computer.
- In remote, we can see the history uploaded to another Git server.

### 2. Terminologies in Git
- `repository` : a folder with my files on it being tracked by Git
- `commit` : a comment we have to write every time we save a file
- `branch` : a copy of the code from the master branch not to break the master branch


### 3. Git vs Github
- Git is a version control system.
- Github is a remote version control website.

### 4. HTML and CSS
- HTML is a markup language that tells the browser what the elements are.
- CSS is a styling language that tells the browser how the elements look.

----

## Module 2. HTML5

### 1. What HTML is
- HTML is hyper text markup language that tells what each element mean.
- HTML document consists of a lot of tags.
- A Web Server searches `index.html` file first.


### 2. What a tag is
- A tag looks like this.
```html
<name attribute="value">Content</name>
```
- We should open a tag and close it. But some tags are self-contained tags because they provide information by themselves.
```html
<!--common tags-->
<a href="https://google.com" target="blank">Google</a>
<!--self-contained tags-->
<img src="/CoodingPenguin/img.png" width=80%>
```

### 3. How HTML document looks
- `<html>` : Content inside this tag is a HTML document. You should say to a browser "This is a HTML document!" by using `<!DOCTYPE html>`
- `<head>` :  Give information to the browser about the website. So it's invisible.
- `<body>` : Give contents users can see. So it's visible.

### 4. How to Add Meta Information
We give extra information about the document to the browser by using `<meta>`. We cannot make my own meta tag. There are only some meta tags that the browser can understand.
```html
<!--What language a document is written-->
<meta charset="utf-8">
<!--Explain briefly about content-->
<meta name="description" content="This is my Kakao clone.">
<!--Who writes this document.-->
<meta name="author" content="CoodingPenguin">
```

### 5. Semantic vs NonSemantic Tags
- Semantic tags are meaningful tags like "This is a title", "This is a hyper link" and so on.
- NonSemantic tags don't have any meanings. For example, `<div>` and `<span>` are nonsemantic tags.
- Why we use nonsemantic tags? We use `<div>` and `<span>` when things like boxes are needed. We put some contents inside them.

### 6. Class and ID
To distinguish between same tags, we name those tags.
- **class** : a common name. Tags with the same class name share the same characteristics.
- **id** : a unique name. 

----

## Module 3. CSS3
```
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
- 많은 element들은 box이다.
    - box의 구성
        - content
        - border : 경계
        - padding : border에서 안쪽으로 있는 간격
        - margin : border에서 바깥쪽으로 있는 간격
    - margin과 padding의 간격
        - padding/margin-top/botton/right/left : 00px; // 각 방향
        - padding/margin : 00px; // 모든 방향
        - padding/margin : 00px 00px; // 첫번째는 상하, 두번째는 좌우방향 
        - padding/margin : 00px 00px 00px 00px; // 상우하좌(↑→↓←)방향, 시계방향
    - border
        - width, style, color 속성 부여가 가능함
        - border : <간격> <스타일> <색상>; // 각각 줄 수 있지만 width-style-color 순으로 한 번에 줄 수도 있음.
```

----

## Module 4. Advanced CSS
