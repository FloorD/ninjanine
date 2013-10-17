##Crash Course HTML & CSS

**Every webpage you look at is** written in a language called **HTML**. You can think of HTML as the skeleton that gives every webpage structure. HTML stands for *HyperText Markup Language*. Hypertext means "text with links in it." You know when you visit a website and see a headline and a bunch of paragraphs? A computer can tell the difference between a paragraph and a headline because each has its own HTML tag. 

A *markup language* is a programming language used to make text do more than just sit on a page: it can turn text into images, links, tables, lists, and much more. HTML is the markup language we'll be learning.

**What makes webpages pretty?** That's CSS — short for Cascading Style Sheets. Think of it like skin and makeup that covers the bones of HTML.  

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
 
Let's go through the code we just wrote! The `<!DOCTYPE html>` is just there to show off that this is indeed a HTML document. 

The stuff we'll put between the `<head>` tags will make for the title of the website, and we'll link to our stylesheet from here.  

Everythink in between the `<body>` tags will contain what we'll see in the browser.  
  
Let's add some content, shall we? Beginning with some headers. From big, to big-ish, to smaller, we've got: `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>` and `<h6>`. 

How big are we talking about?  

#Supersaurus (134 feet long)  
##Argentinosaurus (115-130 feet long)  
###Seismosaurus (120+ feet long)  
####Ultrasauros (100+ feet long)  
#####Diplodocus (90 feet long)  
######Brachiosaurus (85 feet long)  

After a header, we can create a paragraph. Paragraphs need opening and closing `<p></p>`: 

```
<body>  
  <h1></h1>  
    <p></p>  
    <h2></h2>  
      <p></p>  
</body>   
``` 

`<em></em>` italic, `<strong></strong>` bold text.  

`src` stands for "source." It tells the `<img>` link where the picture comes from! Images have a crazy tag, it's self-closing! Check it out:   

```
<img src="" />  
```

Additionally, you could link a picture, to for instance, a [Wikipedia page](http://en.wikipedia.org/wiki/Dinosaurs). Here is the HTML you need to do that:


```
<a href=""><img src="" /></a>  
```

####Lists

#####Unordered lists
An unordered list starts with the `<ul>` tag. Each list item starts with the `<li>` tag.  
The list items are marked with bullets (typically small black circles).  

```html
<ul>
  <li></li>
  <li></li>
  <li></li>
</ul>
```

#####Ordered lists

An ordered list starts with the `<ol>` tag. Each list item starts with the `<li>` tag.  
The list items are marked with numbers.  

```html
<ol>
  <li></li>
  <li></li>
  <li></li>
</ol>
```

###Pretty dino's are pretty

```html
<head>
	<link type="text/css" rel="stylesheet" href="stylesheet.css" />
	<title></title>
</head>
```

####Tables, Divs, and Spans 

Tables are defined with the `<table>` tag.  

A table is divided into rows (with the `<tr>` tag), and each row is divided into data cells (with the `<td>` tag). td stands for "table data," and holds the content of a data cell. A ```<td>``` tag can contain text, links, images, lists, forms, other tables, etc.  

```html
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

The `<div>` tag defines a division or a section in an HTML document. The `<div>` tag is used to group block-elements to format them with CSS.  

The `<div>` element is very often used together with CSS, to layout a web page.

#####Align
left  
right  
center  

The `<span>` tag is used to group inline-elements in a document. The `<span>` tag provides no visual change by itself. The `<span>` tag provides a way to add a hook to a part of a text or a part of a document.

When a text is hooked in a `<span>` element, you can style it with CSS, or manipulate it with JavaScript.  

###CSS

Our stylesheet defines where HTML elements should go, what color they should be, how big they should be, and more. Open your texteditor and create a file called `style.css`.
A style sheet is a file that describes how an HTML file should look. That's it!

We say these style sheets are cascading because the sheets can apply formatting when more than one style applies. For instance, if you say all paragraphs should have blue font, but you specifically single out one paragraph to have red font, CSS can do that! 
There are two main reasons for separating your form/formatting (CSS) from your functional content/structure (HTML):  

- You can apply the same formatting to several HTML elements (using inline styling) without rewriting code (e.g. `style="color:red"`) over and over  
- You can apply similar appearance and formatting to several HTML pages from a single CSS file  

The general format looks like this:  

```
selector {  
    property: value;  
}  
```

A selector can be any HTML element, such as `<p>`, `<img>`, or `<table>`. You just take off the `<>`s! To make a paragraph's text red with CSS, you'd type:

```
p {
    color: red;
}
```

A property is an aspect of a selector. For instance, you can change the font-family, color, and font-size of the text on your web pages (in addition to many more).
You can set many properties for one selector.

A value is a possible setting for a property. color can be red, blue, black, or almost any color; font-family can be a whole bunch of different fonts; and so on.

You need to end each property-value with a semi-colon (;). That's how CSS knows you're done with one pair and ready for the next.

Does CSS know all colors? Nah. It can, however, understand millions of colors in the form of hexadecimal values.  Hexa-what? Each digit can be the numbers 0 through 9 or the letters a through f. Search for "hex color palette" or "hex color picker" with your favorite web browser to find a bunch of options!

Hex values always start with a pound sign (#), are up to six "digits" long, and are case-insensitive: that is, they don't care about capitalization.
   
```
h1 {  
	color: #8B1C62;  
}  
```

HTML comments look like this:
    
```
<!--I'm a comment!-->  
```

CSS comments, on the other hand, look like this:
  
```
/*I'm a comment!*/  
```

When you adjust your font size, you're probably thinking of using `px` (for "pixels"), like so:

A pixel is a dot on your computer screen. Specifying font sizes in pixels is great when you want the user to see exactly on their screen what you designed on yours, though it assumes your screens are of similar size.

What if the user is using a screen that's a very different size from yours, though (like a smartphone screen)? Enter *ems*. The font-size unit *em* is a relative measure: one *em* is equal to the default font size on whatever screen the user is using. 

**serif**: A font with little decorative bits on the ends of the strokes that make up letters. Do a search on "serif" to see what we mean.  

**sans-serif**: A plain-looking font, like this one. It doesn't have the little doohickies on the ends of letters like a serif font does.  

**cursive**: A scripty font! It looks like cursive writing.  


####Buttons!!

:truck: Add a link to your HTML page using `<a></a>` tags, and be sure you include a `href` attribute. Your link can go anywhere!

:truck: On the CSS tab, change your link's `text-decoration` to `none` and its `color` to `#cc0000`.

`border-radius` modifies the corners of HTML objects; it's how you get those cool rounded buttons!

:truck: Set your `div`'s `border-radius` to 5px.

####CSS Classes and IDs
```id```s are to be used only once in your HTML layout. Classes can be used multiple times. Generally ```id```s are used for the main elements of the page, such as header, main content, sidebar, footer, etc. Classes are used for elements that will appear several times on your page, but can not be covered by standard HTML elements. 

* `background-color`, which you set to a named color or hex value
* `height` and `width` which you set to a value in pixels 

####CSS Element Positioning

When you put some text in a box (or, "content in a container"), you may want some control over how far from the edges of the box that content should render. Margins, padding and borders let you do that.

A neat visualization of that is included in many browsers' Web inspector panel. [Firefox has a Page Inspector](https://developer.mozilla.org/en-US/docs/Tools/Page_Inspector), which has an HTML tab. 

#####margins
#####padding
#####borders

