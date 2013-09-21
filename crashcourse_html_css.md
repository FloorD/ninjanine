###Crash Course HTML & CSS

Every webpage you look at is written in a language called HTML. You can think of HTML as the skeleton that gives every webpage structure. HTML stands for HyperText Markup Language. Hypertext means "text with links in it."

A markup language is a programming language used to make text do more than just sit on a page: it can turn text into images, links, tables, lists, and much more. HTML is the markup language we'll be learning. What makes webpages pretty? That's CSS—Cascading Style Sheets. Think of it like skin and makeup that covers the bones of HTML.  

###HTML dinosaurs

We're going to create a simple website about dinosaurs. Ready? The first thing we should do is set up the skeleton of the page. Open your texteditor and paste in: 

```
<!DOCTYPE html>  
<html>  
  <head>  
    <title>  
    </title>  
  </head>  
  <body>  
  </body>  
</html>  
```  

... and save the document as index.html.  

Notice how every element has an opening and a closing tag (the things between angle brackets)? Cool, then you got the basics of HTML syntax!  
Let's go through the code we just wrote! The ``` <!DOCTYPE html> ``` is just there to show off that this is indeed a HTML document. 
The stuff we'll put between the ```<head>``` tags will make for the title of the website, and we'll link to our stylesheet from here.  
Everythink in between the ```<body>``` tags will contain what we'll see in the browser.  
  
Let's add some content, shall we? Beginning with some headers. From big, to big-ish, to smaller, we've got: ```<h1>```, ```<h2>```, ```<h3>```, ```<h4>```, ```<h5>``` and ```<h6>```. How big are we talking about?  

#Supersaurus (134 feet long)  
##Argentinosaurus (115-130 feet long)  
###Seismosaurus (120+ feet long)  
####Ultrasauros (100+ feet long)  
#####Diplodocus (90 feet long)  
######Brachiosaurus (85 feet long)  

After a header, we can create a paragraph. Paragraphs need opening and closing ```<p></p>```: 

```
<body>  
  <h1></h1>  
    <p></p>  
    <h2></h2>  
      <p></p>  
</body>   
``` 


```src``` stands for "source." It tells the ```<img>``` link where the picture comes from!  

```
<img src="" />  
```

Additionally, you could link a picture, to for instance, a [Wikipedia page](http://en.wikipedia.org/wiki/Dinosaurs).

```
<a href=""><img src="" /></a>  
```

####Lists

#####Unordered lists
An unordered list starts with the ```<ul>```` tag. Each list item starts with the ```<li>``` tag.  
The list items are marked with bullets (typically small black circles).  

```
<ul>
<li></li>
<li></li>
<li></li>
</ul>
```

#####Ordered lists
An ordered list starts with the ```<ol>``` tag. Each list item starts with the ```<li>``` tag.  
The list items are marked with numbers.  

```
<ol>
<li></li>
<li></li>
<li></li>
</ol>
```

###Pretty dino's are pretty

```
<head>
	<link type="text/css" rel="stylesheet" href="stylesheet.css" />
	<title></title>
</head>
```

####Tables, Divs, and Spans 

Tables are defined with the ```<table>``` tag.  

A table is divided into rows (with the ```<tr>``` tag), and each row is divided into data cells (with the ```<td>``` tag). td stands for "table data," and holds the content of a data cell. A ```<td>``` tag can contain text, links, images, lists, forms, other tables, etc.  

```
<table border="1">
<tr>
<th>Header 1</th>
<th>Header 2</th>
</tr>
<tr>
<td>row 1, cell 1</td>
<td>row 1, cell 2</td>
</tr>
<tr>
<td>row 2, cell 1</td>
<td>row 2, cell 2</td>
</tr>
</table>   
```

The ```<div>``` tag defines a division or a section in an HTML document. The ```<div>``` tag is used to group block-elements to format them with CSS.  
The ```<div>``` element is very often used together with CSS, to layout a web page.

#####Align
left  
right  
center  

The ```<span>``` tag is used to group inline-elements in a document. The ```<span>``` tag provides no visual change by itself. The ```<span>``` tag provides a way to add a hook to a part of a text or a part of a document.
When a text is hooked in a ```<span>``` element, you can style it with CSS, or manipulate it with JavaScript.  

###CSS

Our stylesheet defines where HTML elements should go, what color they should be, how big they should be, and more. Open your texteditor and create a file called ```style.css```.
A style sheet is a file that describes how an HTML file should look. That's it!

We say these style sheets are cascading because the sheets can apply formatting when more than one style applies. For instance, if you say all paragraphs should have blue font, but you specifically single out one paragraph to have red font, CSS can do that! 
There are two main reasons for separating your form/formatting (CSS) from your functional content/structure (HTML):  

- You can apply the same formatting to several HTML elements (using inline styling) without rewriting code (e.g. style="color:red":) over and over  
- You can apply similar appearance and formatting to several HTML pages from a single CSS file  


####Buttons!!
####CSS Classes and IDs


####CSS Element Positioning 
