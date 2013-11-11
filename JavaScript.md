
## JavaScript - Vanilla and jQuery

### General

Extension of General conventions

* Use single quotes - This means you do not need to escape double quotes when needed to use HTML 
* Use strict equality checks (===) over abstract equality checks (==)
* 
**Use Vanilla JavaScript where possible**

Example: 

* Use for loops over $.each

### DO NOT's

* **do not** use jQuery to build HTML elements

Example:

	var div = $('<div />');

	var div = '<div></div>;

* **do not** use Javascript in HTML attributes to

Example: 

	<a href="javascript:void(0)" onclick="runMe();">Link</a>


### Documentation

* Use YUI Docs for Documentation - When Documentation is required for a plug-in or suite of functions

### Comments

* Add comments within the code when an explanation is need, or you feel it will help other who may need to come into the code

### Variables

* Always **var** up your variables, to a local scope
* Only use one **var** word to define all your variables in a scope, unless the variable needs to have a YUI Docs comment.

Example: 

	// --- Wrong
	var hello = 'World';
	var world = 'Hello';

	// --- Correct
	var hello = 'World'
	  , world = 'Hello;

	/**
	 * current library version
	 *
	 * @private
	 * @property version
	 * @type {String}
	 * 
	**/
	var version = '1.0.2';


* If you need a global variable bind it to a window object for common use. 

Example: 

	var myApp = {
		hello : 'World'
	}

	window.myApp = myApp;
	

### Spacing

Try and make your code readable, as the minification process will remove all the whitespace and line breaks, the extra spacing to ensure readability is better.

**Exception**

* One exception here is when binding events, see the events section for an example
* Do not use tabs and spaces to align things vertically

Example:

	// --- Wrong
	var a = {
		name 	: 'Matthew',
		age  	: 27,
		job  	: 'Developer',
		company : 'AW2.0'
	};

	// --- Correct
	var a = {
		name : 'Matthew',
		age : 27,
		job : 'Developer',
		company : 'AW2.0'
	};
	

#### Calls

Use spacing to separate calls that contain multiple arguments

Function Example:

	// --- Wrong
	doSomething(x,'help',c);
	callMe( '555' );

	// --- Correct
	doSomething( x, 'help', c );
	callMe('555');


Array Example:

	// --- Wrong
	myArr[ x ];
	myArray[1,2,3,4];

	// --- Correct 
	myArr[x];
	myArray[ 1, 2, 3, 4 ];


#### Functions

Creating Function use spacing around the arguments in all cases

Example:
	
	// --- Wrong 
	function hello (x,y,z){}	
	function hello(x) {}

	// --- Correct 
	function hello( x, y, z ) {
		doStuff(x);
	}

	function hello( x ) {
		doStuff(x);
	}


#### IF

* Space after the word **if** and between **)** and **{**
* **} else {** lives on a line of it own

Example:

	// --- Wrong
	if(x){ doSomething() } else { somethingElse() }

	if(x) { hi() } 
	else { boo() }

	// --- Correct
	if ( x ) {
		doSomething();
	} else {
		somethingElse();
	}


#### FOR

* Space after the word **for** and after the end bracket **)** and before first curly bracket **{**
* Spacing after the opening bracket **(** and before the closing bracket **)**

Example:
	
	// --- Wrong
	for(var x=0; x<d.length;x++) { 
	 doSomething();
	}

	// --- Correct
	for ( var x=0; x<d.length; x++ ) {
		doSomething();
	}


### Selectors

* Select elements as direct as possible
* Use ID's to select elements when possible

Example ( Selecting a button with class add ):

	// --- Wrong
	$('.add')
	
	// --- Better
	$('button.add')
	
### Events

* Similar to selectors, bind events to ID's where possible
* Bind events in groups of selectors where possible
* Avoid binding events to the document where possible 
	* 	If you need a live event try to use the most parent element possible

Group Bindings Example:

	<ul id="nav">
		<li><a href="#add" class="add>Add</a></li>
		<li><a href="#delete" class="delete">Delete</a></li>
	</ul>

	// --- Wrong
	$('#nav').on('click', '.add', function(e) {
		e.preventDefault();
		// --- Do your logic for add link
	});

	$('ul').on('click', '.delete', function(e) {
		e.preventDefault();
		// --- Do your logic for delete link
	});

	// --- Better
	$('#nav').on('click', 'li a', function(e) {
		e.preventDefault();
		// --- Do your logic for all links
	});

