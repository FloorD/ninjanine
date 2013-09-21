###Crash Course HTML & CSS

Every webpage you look at is written in a language called HTML. You can think of HTML as the skeleton that gives every webpage structure. HTML stands for HyperText Markup Language. Hypertext means "text with links in it."

A markup language is a programming language used to make text do more than just sit on a page: it can turn text into images, links, tables, lists, and much more. HTML is the markup language we'll be learning. What makes webpages pretty? That's CSS—Cascading Style Sheets. Think of it like skin and makeup that covers the bones of HTML.  

####featuring: dinosaurs!

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
####Tables, Divs, and Spans 
####Buttons!!
####CSS Classes and IDs 
####CSS Element Positioning 
