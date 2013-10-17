##Crash Course JavaScript

JavaScript makes websites respond to user interaction, plus you can use it to build apps and games, access information on the Internet and organize and present data. Let's just say that at the moment something changes on a page without you clicking on something, it's **probably** JavaScript at work. Like when your Facebook Timeline updates or Google autocompletes your search term. 

``` "yourName".length ```   
``` 3 + 4 ```  
``` 3 / 4 ```  

``` "yourName".length * 9 ```  

There are some things you can't do in the console. If you use words that aren't in the JavaScript language, it will get confused and give you an error.  

``` // This is a comment that the computer will ignore. ```   


##You are awesome!
These boxes can be used on websites to confirm things with users. You've probably seen them pop up when you try to delete important things or leave a website with unsaved changes.  
``` confirm("I am awesome!"); ```  

To do any of these actions, the program needs an input. You can ask for input with a prompt:  
``` prompt("What is your name?"); ```

... note the little input field? I bet you've seen that somewhere before ;)

Numbers are quantities, just like you're used to. You can do math with them. Strings are sequences of characters, like the letters a-z, spaces, and even numbers. 
To write a string, surround the string with quotes: "What is your name?"

The third type of data is a boolean (just say "bool-ee-un"). A boolean can have only two values, true or false.  

10 > 3 evaluates to true  
5 < 4 is just crazy talk, so it evaluates to false  

Try it:  
``` "I'm awesome!".length > 10 ```  

##console.log("Hello")

console.log() will take whatever is inside the parentheses and log it (print it out) to the console below your code. 
console.log("Hello")


List of comparison operators:
``` > ``` Greater than  
``` < ``` Less than  
``` <= ``` Less than or equal to  
``` >= ``` Greater than or equal to  
``` === ``` Equal to  
``` !== ``` Not equal to  

Remember: = is for assignment, and === is to check if things are equal!  

You can use comparisons plus booleans to decide whether a block of code should run. This is called an **if statement** or **conditional statement**. *If* the condition (for instance, ```100 < 2```) is true, then it executes the code inside the curly braces {}. If the condition is false, it skips the code in the curly braces entirely and goes on to the next line. Spicing it up at bit: introducing ```else```. If the condition is true, it will execute the code in the first set of curly braces, just like last time. This will skip the else block. But if the condition is false, the robot will skip the first block and execute block after else:  
<pre>
if (this condition is true)  
{  
    // do this  
}  
else // "otherwise"  
{  
    // do this instead  
}  
</pre>

Let's meet an interesting symbol called modulo. When ``` % ``` is placed between two numbers, the computer will divide the first number by the second, and then return the remainder of that division. So if we do ```23 % 10```, we divide 23 by 10 which equals 2 with 3 left over. So ```23 % 10``` evaluates to 3. Is this useful for web development stuff? Not really. So let's move on.  

Sometimes you don't want to display the entire string, just a part of it. For example, in your Gmail inbox, you can set it to display the first 50 or so characters of each message so you can preview them. This preview is a substring of the original string (the entire message). 

``` "some word".substring(x, y) ``` where x is where you start chopping and y is where you finish chopping the original string.

The number part is a little strange. To select for the "he" in "hello", you would write this: ```"hello". substring(0, 2)```;

Think of there being a marker to the left of each character, like this: 0-h-1-e-2-l-3-l-4-o-5.

If you chop at 0 and again at 2 you are left with just he.   

To do more complex coding, we need a way to 'save' the values from our coding. We do this by defining a variable with a specific, case-sensitive name. Once you create (or declare) a variable as having a particular name, you can then call up that value by typing the variable name.

Code:  

``` var varName = data; ```  

Like:  
<pre>
var myAge = 26;  
console.log(myAge);  
</pre>  

And using it:  
``` var myName = "Laura"; ```  

Use console.log to print out the length of the variable myName:  
``` console.log( myName.length ); ```  
Use console.log to print out the first three letters of myName:  
``` console.log( myName.substring(0,3) ); ```  

##Make up your own fairytale 

Remember how...  

<pre>
var myStory = ("Once upon a time...");  
console.log(myStory)  
</pre>
  
Continuing the story you could could use ```if``` and ```else``` statements and let you readers make up their own endings. 

<pre>
var myStory = ("Once upon a time...");  
console.log(myStory)  
if (you want the princess to save the knight)   
{  
  console.log()  
}  
else   
{  
  console.log()  
}  
</pre>


##Functions!!

This is what a function looks like:  
<pre>
var divideByThree = function (number) {  
    var val = number / 3;  
    console.log(val);  
};  
</pre>

Below is the greeting function. We can join strings together using the plus sign ```+```.

<pre>
var greeting = function (name) {  
    console.log("Great to see you," + " " + name);  
};  
alert(greeting("Laura"));  
</pre>

##We're moving!

So far we've only looked at functions with one parameter. But often it is useful to write functions with more than one parameter.  Because we can have more than one parameter, this means we can create more useful functions.   
<pre>
var movingBox = function(length, width) {  
         return length * width;  
};  
</pre>

Of course other parameter values can be used!  

##Going global
We need to be introduced to a super important concept: scope. Scope can be global or local.

Variables defined outside a function are accessible anywhere once they have been declared. They are called global variables and their scope is global.

Variables defined within a function are local variables. They cannot be accessed outside of the function.

Check out the code in the editor. Until now you've been using the var keyword without really understanding why. The var keyword creates a new variable in the current scope. 

##For the love of...
<pre>
console.log(1)  
console.log(2)  
console.log(3)  
console.log(4)  
console.log(5)  
</pre>

Instead of manually typing in ``` console.log ``` five times, we can use a ``` for ``` loop to do this.

``` for (var counter = 1; counter < 6; counter++) { ```   
```	console.log(counter);  ```  
``` } ```  

``` i = i + 1 ```  
This has meant we have incremented (increased) the variable i by 1 each time.

Repeat after me:  
1. A more efficient way to code to increment up by 1 is to write ```i++```.
2. We decrement down by 1 by writing ```i--```.
3. We can increment up by any value by writing ```i += x```, where x is how much we want to increment up by. e.g., ```i += 3``` counts up by 3s.
4. We can decrement down by any value by writing ```i -= x```. (See the Hint for more.)
5. Be very careful with your syntax—if you write a loop that can't properly end, it's called an infinite loop. It will crash your browser! Which is fun once. But then it gets annoying.  

##While that is true...  

##Control Flow

##Arrays and Objects

##OMG YOU MADE IT THROUGH
``` confirm("You are awesome!"); ```
