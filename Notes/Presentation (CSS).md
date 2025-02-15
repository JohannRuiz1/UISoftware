
### CSS Syntax

- h1 {color: blue; font-size: 12px; }
- h1 is selector
- color and font-size are properties
- blue and value are values
- color: blue, font-size: 12px is a declaration 

### Cascading (Order of Priority) 
- Importance
	- Important (!important) -> normal declarations
- Origin 
	- User -> author -> user agent
- Type
	- Inline -> embedded -> external
- Specificity
	- ID -> class -> element
- Source order
	- Later in document -> earlier in document

### Referring to elements
- ID
	- Most specific; can refer to only one element per page
	- HTML attribute: id="id_goes_here"
- Class
	- Used to refer to a group of elements
	- Can be applied to different tag types
	- HTML attribute: class="class_name_goes here"
- Tag
	- Least specific; refers to every element of this tag type
### Inheritance
- Styles applied to a parent element are inherited by (passed down to) child elements
- Some priorities inherited automatically
	- font-family, font-size
- Others can be manually inherited 
```
p {
	color: red;
}	
p a:link {
	color: inherit;
}
```

### Selectors
- Common
	- Descendent: `p span`
	- Child: `p > span`
	- Class: `p.class`
	- ID: `p#id`
- Less common (new in CSS3)
	- Sibling: p + span
	- Match attribute: `input[type="submit"]`
- Child chaining
	- `div h1 p span a i...`
### Box model
![[Pasted image 20250214093310.png]]
### Page layout
- Block vs. inline elements
	- Block span the whole page
	- Inline will line up next to each other, and inline elements can only include inline elements
- Fixed vs. liquid layouts
	- Fixed doesn't change, liquid can change based on device
- `float` and `clear
- Tables for page layout: pros and cons

### Styles types
```
External (prefer)
<link rel="stylesheet" type="text/css" href="styles.css" />

Embdedded
<style type="text/css">
	p {
		width: 30em;
	}
</style>

Inline (avoid)
<a href="http://ww.google.com" style="font-size" italic;">Google</a>
```
- Stylesheets can (and should) be used by multiple pages in your app
- Seek to abstract and generalizes your styles
- Limit use of embedded and inline styles to exceptions and unique situations


### CSS Reset 