# Road Map

## Getting set up

-   Create an account with the p5 editor: <https://editor.p5js.org>
-   Open an additional browser tab with the p5 reference <https://p5js.org/reference/>

## A - Draw shapes to the canvas

-   Understand the canvas size and coordinate system
-   Explore a variety of shapes (and lines, time permitting)
-   Add color, stroke, lineWeight
-   Lab: Explore the line function (if not yet). Draw your own animal or plant using only shapes. Give it color with fill and stroke. keep it simple, maximum 10 shapes. Save your file (will be using it for next lesson)


<table>

<tr>
<td>Code snippet </td>
<td>Description </td>
<td>Reference</td>
</tr>

<tr>
<td>

```javascript
function setup(){
  ...
  //code goes here
  ...
}
```

</td>
<td>This is a p5.js function that runs only once at the very start of the sketch after pressing "play". This is a great place to set up variables and do other preparatory stuff before the draw loop happens.</td>
</tr>

<tr>
<td>

``` javascript
function draw() {
  ...
  //code goes here
  ...
}
```

</td>
<td>This is a p5.js function that runs continuously (forever) in a loop after the setup function has finished running. The draw loop is a good place to put code that needs repeated execution, like animation elements, etc.</td>
</tr>

<tr>
<td>

```javascript
createCanvas(width, height);
```

</td>
<td>This function is required and creates the canvas onto which your sketch will draw graphics to. The createCanvas function should reside at the start of the setup(){ ... } function, and should only be called once.</td>
</tr>

<tr>
<td>

```javascript
fill( r, g, b );
```

</td>
<td>Fills a shape with color. Takes 3 values each between 0 and 255, one for each color (red, green, blue). Any shapes coming after this function in the code will be filled with the specified color. Adding a fourth value will set transparency</td>
</tr>

<tr>
<td>

```javascript
stroke(r, g, b );
```

</td>
<td>Draws shape edges or lines with color. Takes 3 values each between 0 and 255, one for each color (red, green, blue). Any shape edges or lines coming after this function in the code will be drawn with the specified color. Adding a fourth value will set transparency</td>
</tr>
</table>



<table>
<tr>
<td>

```javascript
circle(x-position, y-position, size)
```

</td>
<td>Draws a circle</td>
<td></td>
</tr>

<tr>
<td>

```javascript
square()
```

</td>
<td>Draws a square</td>
<td></td>
</tr>

<tr>
<td>

```javascript
rect()
```

</td>
<td>Draws a rectangle</td>
<td></td>
</tr>

<tr>
<td>

```javascript
ellipse()
```

</td>
<td>Draws an oval</td>
<td></td>
</tr>

<tr>
<td>

```javascript
triangle()
```

</td>
<td>Draws a triangle</td>
<td></td>
</tr>

<tr>
<td>

```javascript
line()
```

</td>
<td>Draws a line between two points</td>
<td></td>
</tr>

<tr>
<td>

```javascript
arc()
```

</td>
<td>Draws an arc</td>
<td></td>
</tr>

</table>





## B - Create a custom function with parameters

-   Declare/define a function
-   Add parameters to the custom function
-   Use relative values rather than constant values (encapsulation)
-   Call the function in the sketch (for example: use mouse position to create a stamp)
-   Lab: Add a parameter to the function to control the size of the output


<table>

<tr>
<td>Code snippet </td>
<td>Description </td>
<td>Reference</td>
</tr>


<tr>
<td>

```javascript
function myFunctionName () {
  ...
  //code goes here
  ...
}
```

</td>
<td>This is the standard format for declaring a function. The "function" keyword is required before writing the name of the function which is then followed by open and closed parenthesis and then open and closed squiggly brackets ( {} ). This function does not use any parameters.</td>
</tr>


<tr>
<td>

```javascript
function myFunctionName ( parameter1, parameter2, etc ) {
  ...
  //code goes here
  ...
}
```

</td>
<td>This function uses a few parameters, and they are required in order for the function to perform its duties. The parameters pass external data into the function and are used within the body of the function in a variety of ways. Parameters can be integers, or strings, or anything really.</td>
</tr>

<tr>
<td>

```javascript
mouseX
```

and

```javascript
mouseY
```

</td>
<td>These are variables that hold the current x-position and y-position of the mouse cursor when it is over the canvas. They are built-in variables, meaning that they exist as part of the p5.js library whether you use them or not, they are always available.</td>
</tr>

</table




## C - Declaring and using variables (and Constants)

-   Add variables to the sketch by declaring at the top using the `let` keyword
-   change the variable using math operators + - \* /
-   Explore strings vs numbers (floats and ints)
-   Console.log to see the value of the variable
-   text() to write it to screen at a given position
-   Lab:

<table>

<tr>
<td>Code snippet </td>
<td>Description </td>
<td>Reference</td>
</tr>

<tr>
<td>

`const`

</td>
<td>The value of a constant can't be changed. A value needs to be assigned to it at the moment it is declared. If you try to change the value of it after declaring, the sketch with throw an error. [link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const)</td>
</tr>

<tr>
<td>

`let`

</td>
<td>"let" is a keyword used to declare a variable. The declared variable exists only within the block that it exists in, not outside of it. </td>
<td>[link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let)</td>
</tr>

<tr>
<td>

`string`

</td>
<td>A string is generally a string of text. Strings require quotation marks (like this: "my string"). Two strings can be added together into a larger string.</td>
<td> [link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)</td>
</tr>

<tr>
<td>

`number`

</td>
<td>Numbers can be of two different types. Whole numbers (known as an "integer"), and numbers with a floating point aka decimal point (known as a "float").</td>
<td>[link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#number_type)</td>
</tr>

<tr>
<td>

```javascript
console.log( put_variable_here );
```

</td>
<td>Logging things to the console is a way to see the value of variables, generally for debugging purposes etc.</td>
</tr>

<tr>
<td>

```javascript
text( value, x-position, y-position)
```

</td>
<td>Draws the value as text onto the canvas at the given x and y coordinates.</td>
</tr>
</table>


## D - Booleans and conditional statements

-   true/false (1's and 0's)
-   If/else if/else statements, aka conditionals
-   mouseClicked events, keyPressed events
-   Use the if/else to call a custom function based on mouse position
-   Lab: Create an applet that draws different shapes depending on keyPresses and mouse Positions (use custom functions)


<tr>
<td></td>
<td></td>
</tr>


<table>

<tr>
<td>Code snippet </td>
<td>Description </td>
<td>Reference</td>
</tr>

<tr>
<td> boolean </td>
<td>
A boolean is a type of variable that can only be either true or false. The status of the boolean is assigned like this: `myBoolean = true;` or `myBoolean = false;`. It is also possible to assign the number `1` or the number `0` to the boolean variable. `1` is the same as `true` and `0` is the same as `false`
</td>
</tr>

<tr>
<td>

```javascript
function mouseClicked() {
  ...
}
```

</td>
<td>This is a special function that listens for when your mouse is clicked. When so, the code inside this function will run exactly once.</td>
</tr>

<tr>
<td>

```javascript
function keyPressed() {
  ...
}
```

</td>
<td>This is a special function that listens for when your keyboard keys are pressed. When so, the code inside this function will run exactly once. The specific key that was pressed will be automatically stored in the key (p5.js built-in) variable.</td>
</tr>

<tr>
<td>

```javascript
if( condition ){
  ...
}
```

</td>
<td>If the condition is true, the code inside the brackets is executed and the if statement is exited. Otherwise, the sketch moves on to the next thing.</td>
</tr>

<tr>
<td>

```javascript
if( condition ) {
    ...
  } else {
    ...
  }
```

</td>
<td>If the condition is true, the code inside the brackets is executed and the if statement is exited. Otherwise the code inside of the else brackets gets executed and then exited.</td>
</tr>

<tr>
<td>

```javascript
if( condition1 ){
    ...
  } else if( condition2 ) {
    ...
  } else {
    ...
  }
```

</td>
<td>If the condition is true, the code inside the brackets is executed and the if statement is exited. Otherwise it moves to then ext else if statement and checks it. If the second if statement is true, then the code inside its brackets is executed and the if statement exited. Finally, if neither of the preceding if statements are true, then the code inside the else brackets gets exicuted and then exited. </td>
</tr>

</table>


## E - External media (images)

-   preLoad an image into the sketch
-   Displaying the image, altering size and position
-   Image filters and effects
-   Lab: build a collage of images

## F - Arrays

-   Declaring and using Arrays
-   Accessing the elements of the array using bracket notation
-   Selecting the last item and a random item from the array
-   Lab: Build a madlib that uses words stored in an array

## G - Loops (for loop / while loop)

-   Use a for loop to add a bunch of numbers into an array
-   Use a for loop to display each element in an array
-   Use the increment variable to access each array item
    Lab: build an array of values and display them to the screen

## H - Work Day

-   Loop and array practice day
-   Use an array to store mouse positions and display the last 100 using a loop
-   Use an array to draw a row of shapes or lines
    Lab:

## I - P5 transformation tools

-   Transformations using p5
-   Push() Pop()
-   Translate() and rotate()
-   Lab: create a graphical composition that incorporates rotating elements

## J -

-   loading video
-   Playing video
-   sketching on top of the video
    Lab:  

## Algorithms to try - Extra

-   draw random circles within a specific rectangular region on the canvas
-   create a bool that bounces off of the edges of the screen
-   Create starts (or pixels) that fall from the top of the screen
-   Explore recursion - a function that calls itself
-   Create a random walker that moves around the screen autonomously
-   Create a grid of shapes without using a for loop
-   a nested For loop



<!-- 7944
4477 -->
7656
