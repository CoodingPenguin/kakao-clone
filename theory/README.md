# Kakao Clone Theory

[Module 1. The Tools of a Web Developer](#module-1-the-tools-of-a-web-developer)

1. [What Git is](#1-what-git-is)
2. [Terminologies in Git](#2-terminologies-in-git)
3. [Git vs Github](#3-git-vs-github)
4. [HTML and CSS](#4-html-and-css)

[Module 2. HTML5](#module-2-html5)
1. [What HTML is](#1-what-html-is)
2. [What a tag is](#2-what-a-tag-is)
3. [How HTML document looks](#3-how-html-document-looks)
4. [How to Add Meta Information](#4-how-to-add-meta-information)
5. [Semantic vs NonSemantic Tags](#5-semantic-vs-nonsemantic-tags)
6. [Class and ID](#6-class-and-id)

[Module 3. CSS3](#module-3-css3)
1. [How CSS looks](#1-how-css-looks)
2. [Mixing CSS with HTML](#2-mixing-css-with-html)
3. [Box Model](#3-box-model)
4. [Inline vs Block vs Inline Block](#4-inline-vs-block-vs-inline-block)
5. [Position Property](#5-position-property)
6. [Flexbox](#6-flexbox)
7. [Pseudo Selectors](#7-pseudo-selectors)
8. [Element States](#8-element-states)

[Module 4. Advanced CSS](#module-4-advanced-css)
1. [Transitions](#1-transitions)
2. [Transformations](#2-transformations)

---

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

---

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
<img src="/CoodingPenguin/img.png" width="80%" />
```

### 3. How HTML document looks

- `<html>` : Content inside this tag is a HTML document. You should say to a browser "This is a HTML document!" by using `<!DOCTYPE html>`
- `<head>` : Give information to the browser about the website. So it's invisible.
- `<body>` : Give contents users can see. So it's visible.

### 4. How to Add Meta Information

We give extra information about the document to the browser by using `<meta>`. These tags are just information so you can put whatever I want.

```html
<!--What language a document is written-->
<meta charset="utf-8" />
<!--Explain briefly about content-->
<meta name="description" content="This is my Kakao clone." />
<!--Who writes this document.-->
<meta name="author" content="CoodingPenguin" />
```

### 5. Semantic vs NonSemantic Tags

- Semantic tags are meaningful tags like "This is a title", "This is a hyper link" and so on.
- NonSemantic tags don't have any meanings. For example, `<div>` and `<span>` are nonsemantic tags.
- Why we use nonsemantic tags? We use `<div>` and `<span>` when things like boxes are needed. We put some contents inside them.

### 6. Class and ID

To distinguish between same tags, we name those tags.

- **class** : a common name. Tags with the same class name share the same characteristics.
- **id** : a unique name.

---

## Module 3. CSS3

### 1. How CSS looks

- CSS consists of **selector part** and **property part**.
- A selector can be all tag names like `<a>`, `<footer>` and a class name or a id name.
- We select tags we want by **selector** and change **properties** by giving values.

```css
selector (id, class, tag name) {
  property-name: value;
  property-name: value;
  property-name: value;
}
```

### 2. Mixing CSS with HTML

- **inline** : Add `<style>` tag in `<head>`. But if you have many pages and want to change something, you have to change all codes in `<style>`. It's very inefficient.

```html
<!--index.html-->
<head>
  ...
  <style>
    h1 {
      font-size: 35px;
    }
  </style>
  ...
</head>
```

- **external** : Make a `styles.css` file and link into all related html files. Then if you change somthing, all changes are applied.

```html
<!--index.html-->
<head>
  ...
  <link rel="stylesheet" href="styles.css" />
  ...
</head>
```

```css
/*styles.css*/
h1 {
  font-size: 35px;
}
```

### 3. Box Model

<img src="./img/box-model.png" width=80%>

The box model consists of `content`,`padding`,`border`, `margin`.

- `padding` : space from the border of the box to the inside.
- `margin` : space from the border of the box to the outside.
- You can change width, style, color of `border`.

```css
/*padding and margin*/
/*apply to each directions or clockwise*/
.box1 {
  padding-top: 10px;
  padding-bottom: 10px;
  margin-left: 20px;
  margin-right: 20px;
}
.box2 {
  padding: 10px 20px 10px 20px;
}
/*apply to all directions*/
.box3 {
  padding: 10px;
}
/*apply to top/bottom and left/right*/
.box4 {
  padding: 10px 20px;
}
```

```css
/*border*/
/*apply to each properties*/
.box {
  border-width: 5px;
  border-color: red;
  border-style: dashed;
}
/*apply to each properties in one line*/
.box2 {
  border: 5px dashed red;
}
```

### 4. Inline vs Block vs Inline Block

```css
.box {
  background-color: red;
  width: 100px;
  height: 100px;
  border: 2px solid black;
  display: block;
}
```

- A box should be a **block** or **inline-block**. The default value is **block**.
- `block` : Blocks do not allow elements next to them.
- `inline-block` : Inline blocks allow elements next to them.
- `inline` : It removes all properties. It's not a box anymore. It's just **text**. So only the length of content exists.

### 5. Position Property

- `position: static` : default value.
- `position: fixed` : It stays with me while I scroll. You can change its location by changing `top`, `bottom`, `left`, `right` values.
- `position: absolute` : It looks for the closest `relative` parent. If not, it aligns to the `<body>`

### 6. Flexbox

We use **Flexbox** to align elements automatically. There are some properties to align elements. To make flex boxes, we have to make a container called **father** and make it flex. Also a flex children can also be a flex father at the same time.

|Properties|What it does|Extra Info|
|:-----:|:-----|:-----|
|`justify-content`|In default, it aligns elements horizontally.|If `flex-direction: column`, it aligns them vertically.|
|`align-items`|In default, it aligns elements vertically.|If `flex-direction: column`, it aligns them horizontally.|
|`flex-direction`|It determines the direction that elements should be aligned.|• `row` is **left-to-right**, `row-reverse` is **right-to-left**.<br/>• `column` is **top-to-bottom**, `column-reverse` is **bottom-to-top**.</br>• If we use value including `reverse`, the start and end of elements are reversed.|
|`order`|0 in default. It determines orders of elements.||
|`align-self`|It applys to specific elements.||
|`flex-wrap`|It determines if we align elements in one line or several lines.|`nowrap` is in **one line**, `wrap` is in **several lines**, `wrap-reverse` is in **several lines reversely**.|
|`flex-flow`|It is a combination of `flex-direction` and `flex-wrap`.||
|`align-content`|It adjusts the line spacing between lines.||

### 7. Pseudo Selectors

pseudo-selector is a way to select elements without using tag names, id or class.

**1. using attributes**

```css
input[required="required"] {
  background-color: pink;
}
```

**2. using the order of elements**

```css
.box:last-child {
  background-color: red;
}
.box:nth-child(2) {
  background-color: yellow;
}
.box:nth-child(3n + 1) {
  background-color: green;
}
```

**3. using the hierarchy of tags**

```css
/* siblings */
.box + .input {
  background-color: red;
}
/* parent-child */
.box > .input {
  background-color: red;
}
```

### 8. Element States

- `hover` : applies to the element which the mouse is over.
- `active` : applies to the element which I'm clicking on.
- `focus` : applies to the element, usually `input` which I'm writing on.
- `visited` : applies to links that have been clicked.

---

## Module 4. Advanced CSS

### 1. Transitions
We use transitions to animate the CSS changes of an element. You have to write a transition property like `transition: [property] [time] ease-in-out`. You can see more about transition in [here](https://developer.mozilla.org/en-US/docs/Web/CSS/transition).
```css
.box{
  color: white;
  background-color: red;
  transition: all 4s ease-in-out;
}
.box:hover{
  color: black;
  background-color: yellow;
}
```

### 2. Transformations
By using transformations, you can rotate, translate, skew an element. But if you want to animate a transformation, you should use a transition. You can see CSS transform examples in [here](https://developer.mozilla.org/en-US/docs/Web/CSS/transform).
```css
.box{
  background-color: white;
  transition: transform 4s ease-in-out;
}
.box:hover{
  transform: rotate(1turn) scale(2, 2);
}
```


[go back to the top](#kakao-clone-theory)