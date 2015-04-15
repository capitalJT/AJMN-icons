#AJMN Icons#

AJMN Icons are the official Icons for the Al Jazeera Media Network.

###What's Included?###

- SVG versions of all icons
- Web fonts in the following formats: eot, svg, ttf, woff
- SVG sprite

###Usage###

Reference the stylesheet:

    <link href="css/font.css" rel="stylesheet">

Create an element which will use the icon:

    <div></div>

Add a class referencing the `icon` stylesheet and specific icon `icon-ajmn-alert`, which you can get from the above stylesheet.

    <div class="icon icon-ajmn-alert"></div>

####Character Mapping####

To use character mapping all you have to do is create an element that will use the icon:

		<div></div>

Add the `data-icon` data attribute with the specific character you want to be mapped:

		<div data-icon="a" class"icon"></div>

####HOW TO ADD SVG SPRITE ICONS TO YOUR PROJECT####

Upload the icons.svg file to your server. In our examples below we assume that the sprite file will be available at: `http://yoursite.com/images/icons.svg`

Go to "Icons Reference" and choose an icon that you want to have on your HTML page. Then click and copy its markup to your HTML page. For instance, the markup for a twitter icon could look like this:

		<svg class="icon-twitter"><use xlink:href="#icon-twitter"></use></svg>

Now it's time to add the sprite file URL to the icon markup. In the example below, the URL is /images/icons.svg. So now the twitter icon markup could look like this:

		<svg class="icon-twitter"><use xlink:href="/images/icons.svg#icon-twitter"></use></svg>

Add the code below to the CSS file that you use for your html page:

		[class^="icon-"], [class*=" icon-"] {
	    height: 32px;
	    width: 32px;
	    display: inline-block;
	    fill: currentColor;
		}

You can use `height` and `width` properties to control icon size. To define icon color use `fill` property. Note: `currentColor` keyword inherits the color value of a parent element.

For IE capability you can use a great polyfill: [svg4everybody](https://github.com/jonathantneal/svg4everybody)

__Remember:__ with Icon Cloud you don't have to worry about IE capability, the sprite file and other stuff. We'll take care of all of that for you, just click the "Publish" button and give it a try.

And that's it!