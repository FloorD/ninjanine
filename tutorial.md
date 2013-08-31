###Ninjanine

Today we'll teach you some tips and tricks on how to use the terminal (or: command prompt) to make it appear to non-developer bystanders like you're in the matrix. The terminal is more than a place where you enter commands to your computer. You can count how often a word appears in a single file, pull a random Chuck Norris quote using the Chuck Norris API, post a tweet from there or convert a large number of pictures to thumbnails. Just to name a few things. Plus: you don't need to install anything, as every computer has such a terminal thing. Let's get started:

**Open your terminal**  
and... **open a texteditor** (like [Sublime][1])  

####Interactive Ruby
Type ```irb``` and hit enter and you'll be able to write Ruby code, right in your editor. Run ```exit``` to exit interactive Ruby mode again.  

We can do some basic stuff, like some math. Try it! Type ```2 + 6``` and you'll see! Now that was pretty easy, but ```irb``` can handle more complex stuff too!
Just try:  

``` 4 * 10 ```  
``` 40 / 4 ```  

or:  
``` a = 2 ```  
``` b = 3 ```  
``` a + b ```  

Cool, huh?

####Controlling EVERTHING from the terminal

We have both noticed that using the terminal for EVERYTHING - yes, also when we're just creating a folder to put all are cut cat pictures in - makes you feel really confident with the command line. Give it a try!  

``` mkdir ninjanine ``` 
to make directory  
``` cd ninjanine ```  
to change into directory  
``` cd .. ``` 
to move one directory up  
``` mkdir ninjanine/img ``` 
to create a folder in a folder  
``` rm ninjanine ``` 
to delete a folder or directory  

Another nifty tric: use the arrows on your keyboard to navigate through previous commands. This will save you a looooot of typing!  

####TryRuby

We borrowed this part of the tutorial from [TryRuby][20], if you want to improve your 'terminal fluency' - and get your ninjanine on ;) - make sure to check out that course!  

Type your first name in quotes like this: ```"Laura"```  
Congratulations, you've successfully formed a string from the letters of your name. A string is a set of characters the computer can process.  

To reverse your name, type: ```"Laura".reverse``` (Don't forget the dot!)  
You have used the reverse method on your name!  

Now, let's make the computer count how many letters are in your name: ```"Laura".length```  
Let's multiply your name by 5. ```"Laura" * 5```  

You've used English-language methods like ```reverse``` and symbolic methods like * (the multiplication method.) Methods are actions!  

####Hello, Rails Girls! 

We can make our computer say all kinds of stuff too. Kinda.  
Create a text file called ```hello-railsgirls.rb``` containing the following code:  

``` puts 'Hello Rails Girls' ```  

Save it and run it:  
``` ruby hello-railsgirls.rb ```  

Works, right? You can also run the short ```"hello Rails Girls"``` program without creating a text file at all. This is called a one-liner:  
``` ruby -e "puts 'Hello world'" ```

Or we can use ```irb``` again!  
``` puts "Hello Rails Girls" ```    

Score!  

####Planets!

We can also use IRB again, to greet some planets (because: why not?!).  

``` irb ```  
``` planet = "mars" ```  
``` puts planet ```  

and the terminal will 'print' ```mars```. 

``` puts "hello" + planet ```  

and the terminal will 'print' ```hellomars```. 

``` puts "hello " + planet ```  

Notice the extra space (pun intended) after ```hello```? The terminal will 'print' ```hello mars```. 

``` puts "hello " + planet.upcase + "!" ``` 

and the terminal will 'print' ```hello MARS!```. 

Next we'll create some arrays! Arr-WHAT? Arrays are 'ordered, integer-indexed collections of any object'. Array indexing starts at 0, instead of at 1. A new array can be created by using ```[]```.  

``` planets = ["mars", "pluto", "jupiter"] ```  

a ```puts planets``` will now return the planets in your array, one by one. 
What do you think ```planets.pop(1)``` does?  

... Exactly! It 'pops' one planet out of our array. ```puts planets``` will now return only 2 of the 3 planets we originally put in there.  

Adding a new planet to our array is equally simple:  

``` planets.push("venus") ```  

Phew!  

####Back To The Future

The awesome thing about Ruby is that it knows a LOT of stuff. Let's try to quiz it!  

``` Time.now ``` 

Quite smart, right? It's today's date, indeed! Now try and guess what the following will do.  

``` Time.now.wday ```

That's right, the day of the week! But okay, we knew that too. We could try something a little complicated... Like going back in time! Pick any date you want, and type it into your terminal like this (first the year, then the month, and finally the day):  

``` t = Time.new(1985, 10, 26) ```  

What we just did was save your special date to a variable called t. Now you can, for example, check whether that day was a monday.  

``` t.monday? ```  

Awesome, right?  
If you want to ask your terminal to return the value of your t variable, you can always just type  

```t```

and press Enter.
However, that formatting doesn't look too nice.. Let's strftime the heck out of it! It goes like this:  

``` t.strftime("%A %B %-d %Y") ```

As you can see in your terminal, `%A` will give you the day of the week, `%B` the month, `%-d` the day of the month, and of course `%Y gives you the year. Jippie!  

Now we can take our Delorean and travel back in time :)  

``` puts "Delorean successfully travelling to " + t.strftime("%A %B %-d %Y") + " at 88 mph" ```

We did forget to accelerate though, so here's how you can do that:  

``` 
(0..88).each do |i|
   puts "Delorean accelerating at #{i} km/h"
end 
```

Enjoy travelling back and forth in time!

[1]: http://www.sublimetext.com/
