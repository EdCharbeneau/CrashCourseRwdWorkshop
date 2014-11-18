#Setup

##Clear foundation samples
1. Open index.html for editing
2. Remove all markup between the opening `<body>` tag and the first `<script>` tag.
3. The result should be a `<body>` tag with three `<script>` elements inside.

##Add InlineIpsum
InlineIpsum is a jQuery plugin that will be used to fill in the page with dummy content. InlineIpsum is helpful but not required for responsive web design.

1. "Install" InlineIpsum by copying `jquery.inlineIpsum.min.js` files from `../Resources/InlineIpsum/demo/javascripts` to the javascripts folder `./js`
2. In `index.html` reference the plugin.  
Find `<script src="js/foundation.min.js"></script>` and on the next line add the code below
        
		<script src="js/jquery.inlineIpsum.min.js"></script>

3. Initialize the plugin  
Find `$(document).foundation();` and on the next line add the code below

		$('body *').inlineIpsum();

4. Create a random paragraph of text  
Find `<body>` and on the next line add the code below

		<div>@Html.Ipsum.p()</div>

5. Open index.html in the browser. A page with only a paragraph of random text should appear.
6. Explore the InlineIpsum plugin by changing the newly added line from `@Html.Ipsum.p()` to the example below

		<div>@Html.Ipsum.h1().p().ul()</div>

7. Save index.html and refresh to see how the output changes.

For additional InlineIpsum syntax see: [https://github.com/EdCharbeneau/InlineIpsum](https://github.com/EdCharbeneau/InlineIpsum)