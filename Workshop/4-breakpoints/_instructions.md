#Working breakpoints small, medium, and large

##Add medium layout
1. Open index.html for editing
- Use the medium class to modify the grid elements so that they are divided into 6 units of width when viewed on a medium _tablet_ sized device. To do this add medium-6 to each column.

		<div class="row">
	        <div class="small-12 medium-6 columns">
	        	<!-- Title and Slug -->
				@Html.Ipsum.h1().h4(8)
	        </div>
	    </div>
		<div class="row">
	        <div class="small-12 medium-6 columns">
	        	<!-- Product image -->
				@Html.Ipsum.image(460, 300)
	        </div>
	    </div>

- Open index.html in the browser and resize the browser to see the effect.

##Working with small to medium
1. Continue editing index.html. Add a new row to the **features** section.

		<section id="features">
        	<div class="row">
		
			</div>
		</section>

- Inside the row add an element that will take half of the screen width when viewing from a small device.

		<div class="small-6 columns">
		
		</div>

- Add a paragraph tag with an image placeholder of 300 x 300.

            <div class="small-6 columns">
                <p>@Html.Ipsum.image(300,300)</p>
            </div>

- Repeat this element until there are four, the markup should look like the code below.

	    <section id="features">
		    <div class="row">
		    	<div class="small-6 columns">
		    		<p>@Html.Ipsum.image(300,300)</p>
		    	</div>
		    	<div class="small-6 columns">
		    		<p>@Html.Ipsum.image(300,300)</p>
		    	</div>
		    	<div class="small-6 columns">
			    	<p>@Html.Ipsum.image(300,300)</p>
			    </div>
			    <div class="small-6 columns">
			    	<p>@Html.Ipsum.image(300,300)</p>
			    </div>
			</div>
	    </section>

- Open index.html in the browser and resize the browser to see the effect.

- Use the medium class to modify the grid elements so that they are divided into 3 units of width when viewed on a medium _tablet_ sized device. To do this add medium-3 to each column.


	    <div class="small-6 medium-3 columns">
	        <p>@Html.Ipsum.image(300,300)</p>
	    </div>
	    <div class="small-6 medium-3 columns">
	        <p>@Html.Ipsum.image(300,300)</p>
	    </div>
	    <div class="small-6 medium-3 columns">
	        <p>@Html.Ipsum.image(300,300)</p>
	    </div>
	    <div class="small-6 medium-3 columns">
	        <p>@Html.Ipsum.image(300,300)</p>
	    </div>


- Open index.html in the browser and resize the browser to see the effect.

##Working with small to large
1. Continue editing index.html. Add a new row to the **benefits** section.

		<section id="benefits">
        	<div class="row">
		
			</div>
		</section>

- Inside the row add an element that will be:
	- Full width on a small device
	- 6 units width on a medium device
	- 8 units width on a large device
	- Inside the element add a few lines of placeholder text.

			<div class="small-12 medium-6 large-8 columns">
				@Html.Ipsum.h3().p().h4().p().h4().p()
			</div>

- On the next line add another element that will be:
	- Full width on a small device
	- 6 units width on a medium device
	- 8 units width on a large device
	- Inside the element add a few lines of placeholder text.
	- Add a call to action

			<div class="small-12 medium-6 large-4 columns">
				@Html.Ipsum.h3().p()
				<p class="text-center">
					<a href="#" class="button">Primary Action</a>
				</p>
			</div>

- Open index.html in the browser and resize the browser to see the effect.