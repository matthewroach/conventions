**The file you are editing should look like one person has created it. This makes it as easy as possible for developers to read and edit each other’s code. Following the coding standards detailed below ensures that.**

Try and make your code readable, as the minification process will remove all the whitespace and line breaks, use extra spacing to ensure readability.

---

Keep line length to a maximum of 120 characters - aim for between 80-100, don’t be afraid of the enter key - This makes readability easier for IDE’s and Version control compares.

## Indentation
* Indentation is your best friend.
* Indent by tabs
* Never double indent a line

## Whitespace
* 3 blank lines between functions
* Newline at end of a file
* Remove all trailing whitespace
* Do not use whitespace to align things up, eg. variables, struct keys/values.
* No whitespace at the end of a line or on blank lines
    * If you use Sublime Text, there is a setting for this: 
```
"trim_trailing_white_space_on_save": true
```

## Naming Variables
* Use camelCase for variable names
* Prefix function arguments with an underscore
* One variable per a line

## Comments
* Start the file with a brief comment explaining contents, the comment at the top of the file should include
    * SVN Id tag
    * @Description:
* Comment where possible, and when you feel an explanation will help others, but don’t go overboard and comment every line. 
* Comment block before each function/block, containing function name and brief description of what the function or block of code does.

### Example JS / CFScript Comment Block: 
``` language-javascript
/**
 *
 * $Id: $
 *
 * @Description: I am a set of common JavaScript / jQuery functions and items used on multiple pages
 *
**/
```

### Example SCSS Comment Block:
``` language-javascript
// 
// $Id: $
//
// @Description: SASS reusable modules
//
```

### JS and SCSS Inline Comment - If more than one line use comment block
``` language-javascript
// Overwrite the clean button style for this area
```

### Example CFML Comment
``` language-javascript
<!---

 $Id: $

 @Description: 

--->
```
