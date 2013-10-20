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

``` for(var i = start; i < end; i++){ ```  
```     // Do something ```  
``` } ```  

Repeat after me:  
1. A more efficient way to code to increment up by 1 is to write ```i++```.
2. We decrement down by 1 by writing ```i--```.
3. We can increment up by any value by writing ```i += x```, where x is how much we want to increment up by. e.g., ```i += 3``` counts up by 3s.
4. We can decrement down by any value by writing ```i -= x```. (See the Hint for more.)
5. Be very careful with your syntax—if you write a loop that can't properly end, it's called an infinite loop. It will crash your browser! Which is fun once. But then it gets annoying.  

##While that is all good and well...  

What if you don't know ahead of time what your counter will be or how many times you'll have to go through the loop? Then ``` while ``` comes in handy!  
The computer could randomly flip a coin and while the coin comes up heads (when coin equalled 1), it would flip again, and it would stop flipping once it got tails (when coin was 0).  
As long as the condition evaluates to true, the loop will continue to run. As soon as it's false, it'll stop. (When you use a number in a condition, as we did earlier, JavaScript understands 1 to mean true and 0 to mean false.)  


``` while(condition){ ```  
```    // Do something! ```  
``` } ```

If you give a while loop a condition that is true and you don't build in a way for that condition to possibly become false, the loop will go on forever and your program will crash. No good!To prevent this from happening, you always need a way to ensure the condition between your while parentheses can change.

Fun fact:  

``` var bool = true; ```  
``` while(bool){ ```  
```     //Do something ```  
``` } ```  

is eactly the same thing as  

``` var bool = true; ```  
``` while(bool === true){ ```  
```     //Do something ```  
``` } ```  

(except for the first one to be way less cluttered, ofcourse).

As we mentioned, for loops are great for doing the same task over and over when you know ahead of time how many times you'll have to repeat the loop. On the other hand, while loops are ideal when you have to loop, but you don't know ahead of time how many times you'll need to loop.



Sometimes you want to make sure your loop runs at least one time no matter what. When this is the case, you want a modified while loop called a do/while loop.

This loop says: "Hey! Do this thing one time, then check the condition to see if we should keep looping." After that, it's just like a normal while: the loop will continue so long as the condition being evaluated is true.

``` loopCondition = false; ```  
  
``` do { ```   
``` 	console.log("I'm gonna stop looping 'cause my condition is " + String(loopCondition) + "!"); ```  	
``` } while (loopCondition); ```  


##Control Flow

``` if (/* Some condition */) { ```   
```     // Do something ```   
``` } else if (/* Some other condition */) { ```   
```     // Do something else ```   
``` } else {    // Otherwise ```   
```     // Do a third thing ```   
``` } ```   


###isNaN('leavened, oven-baked flatbread'); // true

a fancy new function: isNaN.

If you call isNaN on something, it checks to see if that thing is not a number. So:

``` isNaN('berry') // => true ```  
``` isNaN(NaN) // => true ```  
``` isNaN(undefined) // => true ```  
``` isNaN(42);  // => false ```  

Be careful: if you call isNaN on a string that looks like a number, like '42', JavaScript will try to help by automatically converting the string '42' to the number 42 and return false (since 42 is a number).

Note that you can't just do

``` isNaN(unicorns); ```  

unless you've already defined the variable unicorns. You can, however, do

``` isNaN("unicorns"); // => true ```  

JavaScript has the switch statement!

switch allows you to preset a number of options (called cases), then check an expression to see if it matches any of them. If there's a match, the program will perform the action for the matching case; if there's no match, it can execute a default option.

``` switch (/*Some expression*/) { ```  
```     case 'option1': ```  
```         // Do something ```  
```         break; ```  
```     case 'option2': ```  
```         // Do something else ```  
```         break; ```  
```     case 'option3': ```  
```         // Do a third thing ```  
```         break; ```  
```     default: ```  
```        // Do yet another thing ```  
``` } ```  

JavaScript will try to match the expression between the switch() parentheses to each case. It will run the code below each case if it finds a match, and will execute the default code if no match is found.

##Smooth operators

So far we've seen how to control our programs given a single condition: whether one variable is equal to a certain value, for instance. But what if we want to check more than one variable?

For this, we'll need logical operators. JavaScript has three: and (&&), or (||), and not (!).


The logical operator and is written in JavaScript like this: &&. It evaluates to true when both expressions are true; if they're not, it evaluates to false.

``` true && true // => true ```  
``` true && false // => false ```  
``` false && true // => false ```  
``` false && false // => false ```  

The logical operator or is written in JavaScript like this: ||. It evaluates to true when one or the other or both expressions are true; if they're not, it evaluates to false.

``` true || true // => true ```  
``` true || false // => true ```  
``` false || true // => true ```  
``` false || false // => false ```  

The logical operator not is written in JavaScript like this: !. It makes true expressions false, and vice-versa.

``` !true // => false ```  
``` !false // => true ```  

##Array-inception!  

``` var array = [1, 2, 3]; ```  

or:  

``` var array = ["Laura", "Andy", "Tony", "Floor"]; ```   

OR you can have a heterogeneous array, which means a mixture of data types, like so:

``` var mix = [42, true, "towel"]; ```   

you can even put other arrays inside arrays. You can make a two-dimensional array by nesting arrays one layer deep, like so:

``` var twoDimensional = [[1, 1], [1, 1]]; ```  
if you really wanted, you could put arrays inside arrays inside arrays for even more dimensions!

Do you remember how you can call stuff like ``` .length ``` on strings? You can do that with arrays as well!  

Sometimes you want arrays that aren't as nice and even as your 3 x 3 two-dimensional array: you may have three elements in the first row, one element in the second row, and two elements in the third row. JavaScript allows those, and they're called jagged arrays.

``` var languages = ["HTML", "CSS", "JavaScript", "Python", "Ruby"]; ```  
``` console.log(languages[2]); ``` 

Time to crack another joke:  
What is this?*  
``` ["hip","hip"] ```  

* Answer: hip hip array!

##Objects
*Coach: Tell something about object-oriented programming (OOP).  

Using objects, we can put our information and the functions that use that information in the same place.
You can also think of objects as combinations of key-value pairs (like arrays), only their keys don't have to be numbers like 0, 1, or 2: they can be strings and variables.

``` var myObject = {}; ```  
```     myObject.key = value; ```  
```     myObject.key = value; ```  
```     myObject.key = value; ```  

There are two ways to create an object: using object literal notation (which is what you just did) and using the object constructor.

Literal notation is just creating an object with curly braces, like this:

``` var myObj = { ```  
```     type: 'fancy', ```  
```     disposition: 'sunny' ```  
``` }; ```  

``` var emptyObj = {}; ```  

When you use the constructor, the syntax looks like this:

``` var myObj = new Object(); ```  

This tells JavaScript: "I want you to make me a new thing, and I want that thing to be an Object.

``` function someObject() { ```  

```   this.someMethod = function() { ```  
```   }; ```  

###Inheritance

In object-oriented programming, inheritance allows one class to see and use the methods and properties of another class. You can think of it as a child being able to use his or her parent's money because the child inherits the money.

Let's say we're dealing with a lot of Penguins. It sure would be nice to create a Penguin class so that perhaps later we can give it some methods unique to a penguin and not confuse it with the Animal class. If you end up reusing a lot of the same code as the Animal class. This goes against the "DRY" principle of programming: Don't Repeat Yourself.

###Object.prototype

##Private party
In JavaScript all properties of an object are automatically public. Public means that they can be accessed outside the class. Think of these properties as the information a class is willing to share.  
what if an object wants to keep some information hidden?

Just as functions can have local variables which can only be accessed from within that function, objects can have private variables. Private variables are pieces of information you do not want to publicly share, and they can only be directly accessed from within the class.

##OMG YOU MADE IT THROUGH
``` confirm("You are awesome!"); ```
