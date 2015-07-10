**The file you are editing should look like one person has created it. This makes it as easy as possible for developers to read and edit each other’s code. Following the coding standards detailed below ensures that.**

---

Just because you can nest don't go wild with it. Sass is lovely to work with. It can make writing CSS much quicker, and keep it looking tidy. But remember it's just rendering CSS at the end of the day. Having lots of nesting means long CSS Selectors, which in turn can catch you out, and also would you write a huge long selector in vanilla CSS?

## Files

* Use a Reset CSS file
* Split CSS into maintainable files. Files should be split into groups of areas/parts of a site. Example (Not a strict guideline):
    * _tables.scss - Would contain the basic table CSS styles used throughout the site
    * _admin.scss - Would contain all the styles for the admin section, at the top of the file you can include the relevant modules/partials needed
* Move reusable code - to either a partial/module or a mixin

## Selectors

* Use hyphens delimited class names and all lowercase
* Maximum selector length of 4 - Watch your nesting!
* One selector per line
* Use classes not ID’s. - Never apply style to an ID as you lose the ability of reusable styling.


## Properties/ Values

* Properties that have vendor prefixes should be in a mixin for maintainability 
* If using @extend - This is to be the first property.
* Order CSS Declaration in alphabetical order.
* Includes to be at the bottom - Leave a line after the last selector and the first `@include`
* Use a semi-colon after all declarations
* Always use four numerical values for margin/padding/ etc : e.g. `margin: 0 0 1% 0;`
* Zero's should appear on their own, eg, `margin: 0;` - not `margin: 0px;`
* Use RGB color values over HEX values
* If using HEX values ensure they are all uppercase and six characters long.
    * Use the Sass nested Properties when you need more than 1 item of the same namespace

### Namespace Example
``` language-css
// Incorrect 
.heading {
	font-size: 20px;
	font-weight: bold;
}
		
// Correct 
.heading {
	font: {
		size: 20px;
		weight: bold;
	}
}
```
