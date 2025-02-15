
### Graceful Degradation
- Design with the highest-end system in mind
- Degrade gracefully if user don't have these specs (latest browser, big monitors, etc)
- Focus on presentation and browsers

### Progressive Enhancement
- Design with low-end systems in mind (Phones, tablets, JS disabled)
- Provide optional enhancements for system that can use them
- Focus on content

### Responsive Web Design (RWD)
- Responsive Web Design is combines the two 
- Builds on CSS media types and fluid layouts
- Philosophy: Design one website that works across most/all devices by responding dynamically to the media that renders it
- Three key components
	- Fluid layouts
	- Media queries
	- Flexible media

### Fluid Layouts
- Using CSS, describe relationships between elements with relative percentages, not hard-coded pixel values
- Golden rule: result = target / context
```
div.parent {
	width: 300px;
}
div.left-child {
	float: left;
	width: 100px;
}
div.right-child {
	float: right;
	width: 200px;
}
```
```
div.parent {
	width: 300px;
}
div.left-child {
	float: left;
	width: 33.33%;
}
div.right-child {
	float: right;
	width: 66.66%;
}
```

### Media types and queries
- Old school (CSS2): media types
- New school (CSS3): media queries
	- Declaration includes a media type and one or more media queries
	- Queries composed of features and values, connected by logical operators
- In HTML
	- `<link href="styles.css" rel="stylesheet" media="all and (max-width: 1024px)">`
- Within stylesheet
	- `@media all and (max-width: 1024px) {...}`
- Media query features
	- width
	- height
	- orientation (portrait or landscape)
	- aspect-ratio (16/9)
	- resolution
	- color
	- Can add min or max to most of these
- Media query logical operators
	- and 
	- not `@media not screen and (color) {...}`
	- only `@media only screen and (orientation: portrait) {...}`

### Mobile first
- Aim to provide a full-feature mobile experience
- Progressive enhancement 
	- Use media queries to download only what the device will actually use (avoid overwriting)
	- Start with styles for smallest viewport/least bandwidth device and add more as needed
```
@media screen and (min-width: 400px) {...}
@media screen and (min-width: 600px) {...}
@media screen and (min-width: 1000px) {...}
@media screen and (min-width: 1600px) {...}
```

### Flexible media
- Need to resize media to match any resized containers
- For images, can be accomplished with simple CSS3 
```
img {
	max-width: 100%;
}
```
- Doesn't work for embedded media, but workarounds are available

### Device Emulation
- Console Tools let you change to different sizes, orientation, and bandwidths

### RWD framewworks
- Popular example
	- Bootstrap
	- Foundation
- Useful features include
	- Classes for controlling element breakpoints depending on viewport size
	- Classes for showing/hiding elements depending on viewport size
	- Classes for making images responsive