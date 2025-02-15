- W3C Validator to see if we are following web standards
	- https://validator.w3.org

### Doctypes
- Set of rules for what is considered valid markup according to the spec
- No doctype: "quirks mode"
- HTML 4.01
	- Strict, Transitional, Frameset
- XHTML 1.0
	- Strict, Transitional, Frameset
- HTML5 is what we'll use

### HTML5 template
```
<!doctype html>
<html lang="en">
	<head>
		<meta charset="utf-8">
		<title>Document Title</title>
		<link rel="stylesheet" href="css/styles.css">
		<script src="js/scripts.js"></script>
	</head>
	<body>
		<h1> Hello world. </h1>
	</body>
</html>
```

### Semantic Markup
- Choose elements that reflect the type of content they contain
- Common
	- paragraph (p)
	- headings (h1, h2, h3)
	- list (ul and ol, li)
	- anchor (a)
- Less common
	- Quote (q)
	- Citation (cite)
	- Inserted (ins) and deleted (del) text
- Which is semantic?
	- \<b> vs. \<strong>
- Tags that are for presentation instead of content are not semantic

### Block vs. Inline elements
![[Pasted image 20250202192744.png]]