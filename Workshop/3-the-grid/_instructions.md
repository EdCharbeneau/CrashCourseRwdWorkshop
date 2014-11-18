#Working with the grid

##Clear previous samples
1. Open index.html for editing
2. Remove any markup between the opening `<body>` tag and the first `<script>` tag.

##Create sections
Start by creating some sections, this will help outline the document and can be used for styling later on.

1. Find `<body>` and on the next line add the code below

	    <section id="hero"></section>
    	<section id="features"></section>
    	<section id="benefits"></section>
    	<section id="media"></section>

- Inside the hero section add a new grid row

		<div class="row">
        
      	</div>

- Create an element for the smallest possible device by adding an element that will occupy all 12 units of the grid. Inside the row add a div with the class `small-12 columns`. The final markup will look like the code below. This element will contain a title and slug line.

		<div class="row">
	        <div class="small-12 columns">
	        	<!-- Title and Slug -->
	        </div>
	    </div>

- Add the title and slug line by inserting h1 and h4 tag. Specify inlineIpsum to generate 8 words for the h4. 

		<div class="row">
	        <div class="small-12 columns">
	        	<!-- Title and Slug -->
				@Html.Ipsum.h1().h4(8)
	        </div>
	    </div>

- Add an a button below the title and slug line. Wrap the button in a paragraph with the text aligned to center. This will be the primary call to action for the section.

		<div class="row">
	        <div class="small-12 columns">
	        	<!-- Title and Slug -->
				@Html.Ipsum.h1().h4(8)
				<p class="text-center"><a href="#" class="button">Primary Action</a></p>
	        </div>
	    </div>

- Create another element to hold a product image. Again start with the smallest device size. Using inlineIpsum generate a 460 x 300 product photo placeholder inside the new element.

		<div class="row">
	        <div class="small-12 columns">
	        	<!-- Title and Slug -->
				@Html.Ipsum.h1().h4(8)
				<p class="text-center"><a href="#" class="button">Primary Action</a></p>
	        </div>
	        <div class="small-12 columns">
	        	<!-- Product image -->
				@Html.Ipsum.image(460, 300)
	        </div>
	    </div>

- Open index.html in the browser and resize the browser, observe how the page is rendered at different sizes.