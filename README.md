# qtpie.js

### Description

SVG donut chart generated via javascript.

Please note that Jquery is required

### How to use

##### HTML

Create a div in a div with an id and a svg in it with these parameters

```html
<div id="svgPie">
	<div>
		<svg viewbox="0 0 200 200">

		</svg>
	</div>
</div>
```
Add a circle inside the svg.

```html
<div id="svgPie">
	<div>
		<svg viewbox="0 0 200 200">
			<circle transform="translate(100, 100)">
		</svg>
	</div>
</div>
```
For each slice you want, create a path with the attribute data-pie to determine the percentage and the attribute data-desc for th text inside.

```html
<path data-pie="28" data-desc="Photoshop"/>
```

Then add them in the svg, before the circle. With some classes for the color, it will look like this :

```html
<div id="svgPie">
	<div>
		<svg viewbox="0 0 200 200">
			<path class="Photoshop" data-pie="28" data-desc="Photoshop"/>
			<path class="Illustrator" data-pie="7" data-desc="Illustrator"/>
			<path class="InDesign" data-pie="15" data-desc="InDesign"/>
			<path class="HTML5" data-pie="22" data-desc="HTML5"/>
			<path class="CSS3" data-pie="28" data-desc="CSS3"/>
			<circle transform="translate(100, 100)">
		</svg>
	</div>
</div>
```

##### Javascript

Add the link to qtpie.js and the script to init.

```html
<script type="text/javascript" src="assets/js/qtpie.js"></script>
<script>
$(function(){
	qtpie.init();
})
</script>
```

Available parameters are:
- the target id
- the radius of the center (in percent)
- the default word in the middle.
- generation of a list
- activation of hover effect

```html
<script type="text/javascript" src="assets/js/qtpie.js"></script>
<script>
$(function(){
	qtpie.init({
		id         : '#customId', // Default : '#qtpie'
		defaultMsg : 'custom message', // Default : 'Skills'
		radius     : 80, // Default : 70 // note that with 0, you have a pie chart
		list       : true, // Default : 'false'
		hover      : true // Default : 'true'
	});
})
</script>
```

See a demo on [Codepen](http://codepen.io/IceMaD/pen/iKGEq)
