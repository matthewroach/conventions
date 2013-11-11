## CFML

### General

Extension of General conventions

* Declare object at the very beginning of the file

* Use cfscript where possible.
  	* To do all logic at top of .cfm pages
  	* For all CFC's

* CF Tags for page output only. Within HTML Only


* Break CFC's into manageable and grouped functions

* Close non ending tags with **/>**

### Spacing

* Spacing convention the same as JS spacing convention
* Do not use tabs and spaces to align things vertically

Example:

	// --- Wrong
	aObj 		= new api.private.aObj();
	theObject 	= new api.private.theObj();

	// --- Correct
	aObj = new api.private.aObj();
	theObject = new api.private.theObj();


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

Use spacing to separate calls that contain multiple arguments, unless a function is within a function

Function Examples:

	// --- Wrong
	doSomething(x,'help',c);
	callMe( '555' );
	arrayLen(getUser(form.email));

	// --- Correct
	doSomething( x, 'help', c );
	callMe('555');
	arrayLen( getUser(form.email) )


Array Example:

	// --- Wrong
	myArr[ x ];
	myArray[1,2,3,4];

	// --- Correct 
	myArr[x];
	myArray[ 1, 2, 3, 4 ];


#### Functions

* Creating Function use spacing around the arguments in all cases
* Declare the argument type
* Specify a default value when possible

Example:
	
	// --- Wrong 
	function hello (string x, numeric y, struct z=''){}	
	function hello(string x) {}

	// --- Correct 
	function hello( string x, numeric y, struct z='' ) {
		doStuff(x);
	}

	function hello( string x ) {
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
	for(var x=1; x<=arrayLen(foo); x++) { 
	 doSomething();
	}

	// --- Correct
	for ( var x=1; x<=arrayLen(foo); x++ ) {
		doSomething();
	}


## tags

### General

* Use shorthand cfoutput tags when output inside of HTML tags - Requires a recent nightly build
* Use a bit more white space around the tags to break up for easy ready.


### Tags

#### IF

* Space after the word **if** and between **)** and **>**
* Wrap if check in brackets **( )**
* **cfelse** lives on a line of it own
* Leave a line space between CFIF tags if code inside is more than one line

Example:

	// --- Wrong
	<cfif isDefined('session.user')>
		doing something here 
		and here
		ooo and here
 	<cfelse>
		somethingElse
		need done here
		and here
	</cfif>

	<cfif isDefined('session.user')>

		doing something here 

 	<cfelse>

		need done here

	</cfif>


	// --- Correct
	<cfif ( isDefined('session.user') ) >
	
		doing something here 
		and here
		ooo and here
 	
	<cfelse>

		somethingElse
		need done here
		and here

	</cfif>

	<cfif isDefined('session.user')>
		doing something here 
 	<cfelse>
		need done here
	</cfif>