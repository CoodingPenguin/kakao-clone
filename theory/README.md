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
We give extra information about the document to the browser by using `<meta>`. These tags are just information so you can put whatever I want.
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
### 1. How CSS looks
- CSS consists of **selector part** and **property part**.
- A selector can be all tag names like `<a>`, `<footer>` and a class name or a id name.
- We select tags we want by **selector** and change **properties** by giving values. 
```css
selector (id, class, tag name){
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
        h1{
            font-size:35px;
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
    <link rel="stylesheet" href="styles.css">
    ...
</head>
```
```css
/*styles.css*/
h1{
    font-size:35px;
}
```

### 3. Box Model 
<img src="./img/box-model.png" width=80%>

The box model consists of `content`,`padding`,`border`, `margin`.
* `padding` : space from the border of the box to the inside.
* `margin` : space from the border of the box to the outside.
* You can change width, style, color of `border`.
```css
/*padding and margin*/
/*apply to each directions or clockwise*/
.box1{
    padding-top: 10px;
    padding-bottom: 10px;
    margin-left: 20px;
    margin-right: 20px;
}
.box2{
    padding: 10px 20px 10px 20px;
}
/*apply to all directions*/
.box3{
    padding: 10px;
}
/*apply to top/bottom and left/right*/
.box4{
    padding: 10px 20px;
}
```
```css
/*border*/
/*apply to each properties*/
.box{
    border-width: 5px;
    border-color: red;
    border-style: dashed;
}
/*apply to each properties in one line*/
.box2{
    border: 5px dashed red;
}
```

### 4. Inline vs Block vs Inline Block
```css
.box{
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

----

## Module 4. Advanced CSS
