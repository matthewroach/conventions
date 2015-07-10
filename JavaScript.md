**The file you are editing should look like one person has created it. This makes it as easy as possible for developers to read and edit each other’s code. Following the coding standards detailed below ensures that.**

---

Use vanilla JavaScript where possible, for example using native for loops over the $.each()

Use the $aw2 library if you are using jQuery, this provides a consistent style for some common jQuery functions: https://github.com/aw20/coreJS


## General
* Use strict equality checks (===) over abstract equality checks (==)
* Do not use jQuery to build HTML elements, build up the HTML string, 
    * **DO NOT** -  `var div = $('<div />');`
    * **DO** - `var div = '<div></div>';`
* Do not use JavaScript with HTML elements the binding a default prevention should be handled within the JavaScript, eg. 
    * **DO NOT** - `<a href="javascript:void(0)" onclick="runMe();">Link</a>`
    * **DO** - Use JavaScript to attach the event and control it’s behaviour, either preventDefault or return false

## DOM Interactions
* Make as few paint’s to the DOM as possible - If outputting HTML in a for loop build up the string and output after the loop;

``` language-javascript
// Incorrect
for ( var x=0; x<d.length; x++ ) {
    $('body').append('<h1>Hello</h1>');
}

// Correct
var output = '';
for ( var x=0; x<d.length; x++ ) {
	output += '<h1>Hello</h1>';	
}
$('body').append(output);
```

* Reduce interaction to the DOM by caching your selectors, example if you are grabbing data from a form, set the form to a variable, then use the find method to get access to the other data within your function;

``` language-javascript
// Incorrect
data.name = $('#name').val();
data.email = $('#email').val();

// Correct
var $signUp = $('#signup');
data.name = $signUp.find('#name').val();
data.email = $signUp.find('#email').val();
```

## Variables
* Always var up your variables, to a local scope
* Use one var per variable, declared on individual lines.

``` language-javascript
// Incorrect
var myVariable = true
    , anotherVariable = false;

// Correct
var myVariable = true;
var anotherVariable = false;
```

* Bind global variables to the window object, eg.

``` language-javascript
var myApp = {
	hello: 'World'
}

window.myApp = myApp;
```

## Selectors

* Select elements as direct as possible `$('button.add');`
* Use ID's to select elements when possible
* When using jQuery use the find method rather a massive selector string, eg.

``` language-javascript
// Incorrect
$('#element p img');

// Correct
$('#element').find('p img');
```

## Events

* Similar to selectors, bind events to ID's where possible
* Bind events in groups of selectors where possible
* Avoid binding events to the document where possible 
* If you need a live event try to use the most parent element possible

### Group Bindings Example:

``` language-javascript
<ul id="nav">
	<li><a href="#add" class="add>Add</a></li>
	<li><a href="#delete" class="delete">Delete</a></li>
</ul>

// Incorrect
$('#nav').on('click', '.add', function(e) {
	e.preventDefault();
	// --- Do your logic for add link
});

$('ul').on('click', '.delete', function(e) {
	e.preventDefault();
	// --- Do your logic for delete link
});

// Better
$('#nav').on('click', 'a', function(e) {
	e.preventDefault();
	// --- Do your logic for all links here, pass of to a function
});
```

## Functions

* Use spacing around the arguments in all cases
    * space after the word **function**
    * no space between the function name and the opening parenthesis 
    * Space after the opening and closing parenthesis
    * separate the function arguments using a space after the comma
    * space after the last argument
* function arguments to be prefixed with an underscore

### Example:

``` language-javascript
// Incorrect
function hello (x,y,z){}	
function hello(x) {}

// Correct
function hello( _x, _y, _z ) {
	doStuff(_x);
}

function hello( _x ) {
	doStuff(_x);
}
```


## IF

* Space after the word **if** and between **)** and **{**
* **} else {** lives on a line of it own

Do not use shorthand if statements (without the curly brackets).

### Example:

``` language-javascript
// Incorrect
if(x){ doSomething() } else { somethingElse() }

if(x) { hi() } 
else { boo() }

// Correct
if ( x ) {
	doSomething();
} else {
	somethingElse();
}
```


## FOR

* Space after the word for and after the end bracket ) and before first curly bracket {
* Spacing after the opening bracket ( and before the closing bracket )

### Example:

``` language-javascript
// Incorrect
for(var x=0; x<d.length;x++) { 
 doSomething();
}

// Correct
for ( var x=0; x<d.length; x++ ) {
	doSomething();
}
```
