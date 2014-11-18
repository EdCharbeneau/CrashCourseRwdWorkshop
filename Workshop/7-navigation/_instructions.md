#Building a top bar

##Basic top bar
1. Open index.html for editing
2. Locate the opening `<body>` tag. This is where the top bar menu will be added.
3. Below the `<body>` tag add a nav element with the top bar class. Be sure to add the `data-topbar` attribute, this will bind the element to its JavaScript counterpart. Give the nav element a `role="navigation" attribute to assist with screen readers and accessibility.

		<nav class="top-bar" data-topbar role="navigation">
		
		</nav>

- Inside the top bar, and a `<ul>` with the class `title-area`. This is where site branding will be placed.

		<nav class="top-bar" data-topbar role="navigation">
            <ul class="title-area">
             
            </ul>
        </nav>

- Give the `<ul>` a list item with the class `name` 

		<nav class="top-bar" data-topbar role="navigation">
            <ul class="title-area">
                <li class="name">
        
                </li>
        </nav>

- Inside the *name* list item add an `<h1>` with a anchor that has the text *my site*

		<nav class="top-bar" data-topbar role="navigation">
            <ul class="title-area">
                <li class="name">
                    <h1><a href="#">My Site</a></h1>
                </li>
                
            </ul>
        </nav>

- Open index.html in the browser there should be a black bar at the top of the page titled *my site*

- Below the *name* list item, add another list item with the class `toggle-topbar menu-icon`
- Inside the list item create an anchor with that contains a `<span>` with the text *Menu*. This will become the icon shown on a small device that allows the user to expand a hidden menu.

            <ul class="title-area">
                <li class="name">
                    <h1><a href="#">My Site</a></h1>
                </li>
                <li class="toggle-topbar menu-icon"><a href="#"><span>Menu</span></a></li>
            </ul>

- Add a section below the *title-area* element, give it the class `top-bar-section`. All menu items will exist in this section. The section can have both a left and right aligned menu.
		
            <ul class="title-area">
                <li class="name">
                    <h1><a href="#">My Site</a></h1>
                </li>
                <li class="toggle-topbar menu-icon"><a href="#"><span>Menu</span></a></li>
            </ul>

            <section class="top-bar-section">
				<!-- All menu items will go here -->
			</section>

- In the *top-bar-section* add a left menu by creating a `<ul>` with the class `left`
- Give the *left* list three list items containing anchors to the **features**, **benefits**, and **media** sections of content on the page.
				
		<ul class="left">
        	<li><a href="#features">Features</a></li>
            <li><a href="#benefits">Benefits</a></li>
            <li><a href="#media">Media</a></li>
        </ul>

- Open index.html in the browser and resize the browser, observe how the page is rendered at different sizes.

##Call to action
1. Continue editing index.html
- Add a right aligned menu element. Below the *left* `<ul>` add a *right* `<ul>` with the class `right`.

		<ul class="right">
        	
        </ul>

- Add a call to action button to the *right* menu. Inside the *right* `<ul>`, add a list item with the class ``
- Create a button inside the list item with the text *action*

		<ul class="right">
			<li class="has-form">
				<a href="#" class="button">Action</a>
	 		</li>
	 	</ul>

- Open index.html in the browser and resize the browser, observe how the page is rendered at different sizes.

##Aligning with the grid
1. Align the top bar with the rest of the grid. Wrap the entire top bar markup with a `<div>` with the class `contain-to-grid`. The menu will now align with the page content.

		<div class="contain-to-grid">
	        <nav class="top-bar" data-topbar role="navigation">
	            <ul class="title-area">
	                <li class="name">
	                    <h1><a href="#">My Site</a></h1>
	                </li>
	                <li class="toggle-topbar menu-icon"><a href="#"><span>Menu</span></a></li>
	            </ul>
	
	            <section class="top-bar-section">
	                <ul class="left">
	                    <li><a href="#features">Features</a></li>
	                    <li><a href="#benefits">Benefits</a></li>
	                    <li><a href="#media">Media</a></li>
	                </ul>
	                <ul class="right">
	                    <li class="has-form">
	                        <a href="#" class="button">Action</a>
	                    </li>
	                </ul>
	            </section>
	        </nav>
	    </div>

- Open index.html in the browser and resize the browser, observe how the page is rendered at different sizes.