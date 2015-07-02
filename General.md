## General Conventions

**The file you are editing should look like one person has been inside it, take a minute or two to look at the conventions used in the file and abide by them even if you don't like them!**

### Indentation
 
* Indentation is your best friend.
* Indent by tabs
* Never double indent a line
* No whitespace at the end of a line or on blank lines  

### Whitespace

* 3 blank lines between functions
* New line at end of a file
* Remove all trailing white space
	
>	If you use Sublime Text, there is a setting for this:
>	"trim\_trailing\_white\_space\_on\_save": true

### Naming Variables

* Use camelCase for short variable names
* Seperate large variable names with an underscore


### Comments

* Start the file with comment explaining contents
* Comment where possible, and when you feel there is an explanation to help others
* Comment block before each function/block, containing function name and brief description of what the function or block of code does.
	
#### Multi Line Comments:

Leave a line above the first comment line, and below the last line of comment

	/**
	 *
	 * Comment Here
	 * and Here
	 * 
	**/
	
	
	//
	//		Sass Comments Heading Blocks
	//	___________________________________________________________________________

	
	<!---
	 *
 	 * CFML Comment
	 *
	--->

Notice above the space of the at start of line before the asterisk the start and end line are inline then each line is one space in to start the asterisk, then one space after the asterisk to start your comment

#### Single Line Comments

	/* --- CSS Comment Here --- */

	// Sass Comments ( These are not output in compiled output )

	// --- JS Comment / cfscript