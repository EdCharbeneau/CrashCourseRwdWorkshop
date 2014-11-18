#Keeping things even with Block-grid 

Block grids are a way to evenly split contents of a list within the grid. Great for cases when the length of the content is unknown at design time.

##Use block grid to create evenly spaced footer links
1. Open index.html for editing
- After the **media** section and before the first `<script>` tag. Create footer element, inside place a row with an element that will be full width. Inside the element, add an `h4` with the text **Links**. 

	    <footer>
	        <div class="row">
	            <div class="small-12 columns">
	                <h4>Links</h4>

	            </div>
	        </div>
	    </footer>

- After the Links heading, generate an `<ul>` with multiple links as list items `<li><a>Item</a></li>`. Give the `<ul>` a block-grid class that will be 2 for small, 3 for medium, and 4 for large. This can be done using the inlineIpsum generator, or the sample markup can be found below.  
The following script creates 14 list items, 2 words long, with an anchor tag, and the specified class applied to the `<ul>`:

		@Html.Ipsum.ul(14, 2, true, {class: "small-block-grid-2 medium-block-grid-3 large-block-grid-4"})

	**Or:**

		<ul class="small-block-grid-2 medium-block-grid-3 large-block-grid-4">
			<li><a href="#">egestas tellus</a></li>
			<li><a href="#">ligula ullamcorper</a></li>
			<li><a href="#">neque aliquam</a></li>
			<li><a href="#">nisl nunc</a></li>
			<li><a href="#">pulvinar mattis</a></li>
			<li><a href="#">habitant morbi</a></li>
			<li><a href="#">augue neque</a></li>
			<li><a href="#">euismod quis</a></li>
			<li><a href="#">tellus integer</a></li>
			<li><a href="#">sed vulputate</a></li>
			<li><a href="#">est ullamcorper</a></li>
			<li><a href="#">tellus cras</a></li>
			<li><a href="#">eget mi</a></li>
			<li><a href="#">blandit volutpat</a></li>
		</ul>

- Open index.html in the browser and resize the browser, observe how the page is rendered at different sizes.