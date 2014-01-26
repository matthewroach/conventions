## CSS - Using Sass

### Files

* Split CSS into maintainable files
* Move reusable code - to either a partial or a mixin


### Selectors

* Use a Reset
* Use hyphens delimited class names
* One selector per line
* Do not style an ID, use only classes


### Properties / Values

* Order CSS Declaration in alphabetical order
* Vendor prefixes come at the bottom, with -moz first
* Use a semi-colon after all declarations
* Always use four numerical values for margin/padding/ etc : e.g. margin: 0 0 1% 0;
* Use the Sass nested Properties when you need more than 1 item of the same namespace: 

Example: 

	.heading {
		font-size: 20px;
		font-weight: bold;
	}
	
	Becomes ::
		
	.heading {
		font: {
			size: 20px;
			weight: bold;
		}
	}

	
### Sass

Just because you can nest don't go wild with it. Sass is lovely to work with an can make writing CSS much quicker, and keep it looking tidy. But remember it's just rendering CSS at the end of the day. Having lots of nesting means long CSS Selectors, which in turn can catch you out, and also would you write a huge long selector in vanilla CSS?