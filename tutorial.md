###Ninjanine

**Introduction**  

Hej, I'm Laura. I'm originally from Italy, grew up in France, moved to Austria about 13 years ago, and also lived in Norway for a little while.  


Hi. My name is Floor. Two years ago I exchanged Rotterdam for Vienna to work at a startup that used Ruby on Rails. Cool thing is that many of my developer coworkers had coached at Rails Girls events, and I was familiar with their program. I started going though their courses, in August last year, supported by one of my coworkers. I organized Rails Girls Rotterdam in January, organizing [Rails Girls The Hague][1] in September, I co-organize the [Ruby user group meetups in Vienna][2] and the [PyLadies workshops in Vienna][3]. I currently work at [Usersnap][4] and spend the little time that is left coaching at Rails Girls events and helping out where I can when it comes to [Rails Girls Summer of Code][5].


Today we'll teach you some tips and tricks on how to use the terminal (or: command prompt) to make it appear to non-developer bystanders like you're in the matrix. The terminal is more than a place where you enter commands to your computer. You can count how often a word appears in a single file, pull a random Chuck Norris quote using the Chuck Norris API, post a tweet from there or convert a large number of pictures to thumbnails. Just to name a few things. Plus: you don't need to install anything, as every computer has such a terminal thing. Let's get started:

####Interactive Ruby
Type ```irb``` and hit enter and you'll be able to write Ruby code, right in your editor. Run ```exit``` to exit interactive Ruby mode again.  

We can do some basic stuff, like some math. Try it! Type ```2 + 6``` and you'll see! Now that was pretty easy, but ```irb``` can handle more complex stuff too!
Just try:  

```4 * 10```  
```40 / 4```  

or:  
```a = 2```  
```b = 3```  
```a + b```  

Cool, huh?

####Controlling EVERTHING from the terminal

We have both noticed that using the terminal for EVERYTHING - yes, also when we're just creating a folder to put all are cut cat pictures in - makes you feel really confident with the command line. Give it a try!  

```
mkdir ninjanine
``` 
make directory  
```
cd ninjanine
```  
change into directory  
```
cd ..
``` 
moving one directory up  
```
mkdir ninjanine/img
``` 
creating a folder in a folder  
```
rm ninjanine
``` 
deleting a folder or directory  

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

```puts 'Hello Rails Girls'```  

Save it and run it:  
```ruby hello-railsgirls.rb```  

Works, right? You can also run the short ```"hello Rails Girls"``` program without creating a text file at all. This is called a one-liner:  
```ruby -e "puts 'Hello world'"```

Or we can use ```irb``` again!  
```puts "Hello Rails Girls"```    

Score!  

####Planets!

We can also use IRB again, to greet some planets (because: why not?!).  

```
irb
```  
```
planet = "mars"
```  
```
puts planet
```  

and the terminal will 'print' ```mars```. 

```
puts "hello" + planet
```  

and the terminal will 'print' ```hellomars```. 

```
puts "hello " + planet
```  

Notice the extra space (pun intended) after ```hello```? The terminal will 'print' ```hello mars```. 

```
puts "hello " + planet.upcase + "!"
``` 

and the terminal will 'print' ```hello MARS!```. 

Next we'll create some arrays! Arr-WHAT? Arrays are 'ordered, integer-indexed collections of any object'. Array indexing starts at 0, instead of at 1. A new array can be created by using ```[]```.  

```
planets = ["mars", "pluto", "jupiter"]
```  

a ```puts planets``` will now return the planets in your array, one by one. 
What do you think ```planets.pop(1)``` does?  

... Exactly! It 'pops' one planet out of our array. ```puts planets``` will now return only 2 of the 3 planets we originally put in there.  

Adding a new planet to our array is equally simple:  

```
planets.push("venus")
```  

Phew!  

####Back To The Future

The awesome thing about Ruby is that it knows a LOT of stuff. Let's try to quiz it!  

<pre>Time.now</pre>  

Quite smart, right? It's today's date, indeed! Now try and guess what the following will do.  

```
Time.now.wday
```

That's right, the day of the week! But okay, we knew that too. We could try something a little complicated... Like going back in time! Pick any date you want, and type it into your terminal like this (first the year, then the month, and finally the day):  

```
t = Time.new(1986, 05, 01)
```  

What we just did was save your special date to a variable called t. Now you can, for example, check whether that day was a monday.  

```
t.monday?
```  

Awesome, right?  

####Resources

**Laura:**  
-  [Jessie learns to code][14] - tips, tricks, and ranting from a girl learning how to code
-  [Michael Hartl's Ruby on Rails Tutorial][15] - this one's pretty tough for a beginner, but don't give up!
-  [RailsCasts][16] - though the screencasts tend to be pretty specific, they're very useful for getting to know some gems or solving problems.

**Floor:**  
-  [jenniferdewalt.com][6] - building a website a day  
-  [Codecademy.com][7]  
-  [Rails for Zombies][8] - 5 free videos with interactive code quizzes from Code School  
-  [GitImmersion][9] & [TryGit][13] - understanding git  
-  [RubyTapas][10] - Short screencasts twice a week will introduce you to a wide variety of intermediate to advanced Ruby concepts and techniques, as well as core Object-Oriented design principles.  
-  [RubyRogues][11] - You understand about 20% in the beginning, but make sure to pause the episode, look stuff up and you'll get to know the lingo pret-ty fast. 
-  Go to [a Ruby user group][12] and find a mentor!!  


[1]: http://railsgirls.com/thehague
[2]: http://vienna-rb.at
[3]: http://www.meetup.com/PyLadies-Vienna/
[4]: http://usersnap.com
[5]: http://railsgirlssummerofcode.org/

[6]: http://blog.jenniferdewalt.com/
[7]: http://www.codecademy.com/
[8]: http://railsforzombies.org/
[9]: http://gitimmersion.com/
[10]: http://www.rubytapas.com/
[11]: http://rubyrogues.com/
[12]: http://rubyusergroups.org/
[13]: http://www.codeschool.com/courses/try-git

[14]: http://jessiecodes.wordpress.com/
[15]: http://ruby.railstutorial.org/ruby-on-rails-tutorial-book
[16]: http://railscasts.com/

[20]: http://tryruby.org
