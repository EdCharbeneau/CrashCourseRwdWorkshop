#Interchange

Interchange uses media queries to dynamically load responsive content that is appropriate for different users' browsers.

1. Open index.html for editing
2. Locate the *media* section, replace `show-for-medium-up` and `show-for-large-up` with `small-12`

	    <section id="media">
	        <div class="row">
	            <div class="small-12 medium-6 large-4 columns">
	                <div class="flex-video">
	                    <iframe width="1280" height="750" src="http://www.youtube.com/embed/fDSGh8i4hcs" frameborder="0" allowfullscreen></iframe>
	                </div>
	            </div>
	            <div class="small-12 medium-6 large-4 columns">
	                <div class="flex-video">
	                    <iframe width="1280" height="750" src="http://www.youtube.com/embed/BbYnzyvl4Y4" frameborder="0" allowfullscreen></iframe>
	                </div>
	            </div>
	            <div class="show-for-large-up medium-6 large-4 columns">
	                <div class="flex-video">
	                    <iframe width="1280" height="750" src="http://www.youtube.com/embed/YDNmyyrEZho" frameborder="0" allowfullscreen></iframe>
	                </div>
	            </div>
	            <div class="small-12 columns show-for-small-only">
	                <p class="text-center"><a href="#top" class="secondary button expand">top</a></p>
	            </div>
	        </div>
	    </section>

3. Remove the last `<div>` element containing the **top** button

	    <section id="media">
	        <div class="row">
	            <div class="small-12 medium-6 large-4 columns">
	                <div class="flex-video">
	                    <iframe width="1280" height="750" src="http://www.youtube.com/embed/fDSGh8i4hcs" frameborder="0" allowfullscreen></iframe>
	                </div>
	            </div>
	            <div class="small-12 medium-6 large-4 columns">
	                <div class="flex-video">
	                    <iframe width="1280" height="750" src="http://www.youtube.com/embed/BbYnzyvl4Y4" frameborder="0" allowfullscreen></iframe>
	                </div>
	            </div>
	            <div class="show-for-large-up medium-6 large-4 columns">
	                <div class="flex-video">
	                    <iframe width="1280" height="750" src="http://www.youtube.com/embed/YDNmyyrEZho" frameborder="0" allowfullscreen></iframe>
	                </div>
	            </div>
	        </div>
	    </section>

4. Move the **media** content to a "*partial*", copy the **row** element and all elements inside. Paste them in a new file named _media.html.

	    <section id="media">
	        ... moved to _media.html
	    </section>

5. Use interchange to load the partial for large devices, for small devices display a link to a separate media page. *The media page will be created in the next steps.* 
	- Create an interchange placeholder us a `<div>` with the `data-interchange` attribute.
	- Because of browser security when loading external content to a web page, the partial must be hosted. For the purpose of this exercise use the gist url **https://gist.githubusercontent.com/EdCharbeneau/5dc3f64f14511dd41f21/raw/481256a3dc469b6d6a86a6425e74348af8f8f22a/_media.html** This is a hosted version of _media.html created in step 4.

		    <section id="media">
		        <div data-interchange="[https://gist.githubusercontent.com/EdCharbeneau/5dc3f64f14511dd41f21/raw/481256a3dc469b6d6a86a6425e74348af8f8f22a/_media.html, (large)]">
		            <!-- Default content goes here -->
		        </div>
		    </section>
	- Add a link button to the default content that will take the user to **media.html** This element will be displayed when no valid screen sizes are found by interchange. In this case **all** but **large**.
	
		    <section id="media">
		        <div data-interchange="[https://gist.githubusercontent.com/EdCharbeneau/5dc3f64f14511dd41f21/raw/481256a3dc469b6d6a86a6425e74348af8f8f22a/_media.html, (large)]">
		            <!-- Default content goes here -->
					<p class="text-center"><a class="button secondary" href="media.html">View Media</a></p> 
		        </div>
		    </section>

- Modify the menu so that the **media** menu item links to **#media** on large devices, and links to **media.html** for all other devices. To do this use visibility classes.

                <ul class="left">
                    <li><a href="#features">Features</a></li>
                    <li><a href="#benefits">Benefits</a></li>
                    <li class="show-for-large-up"><a href="#media">Media</a></li>
                    <li class="show-for-small-only"><a href="./media.html">Media</a></li>
                </ul>

- Create media page **media.html** that will display only the media elements. This page will be displayed to users with small devices. To expedite the process, this file has already been created */begin/media.html*

- Use interchange to load the partial, this time for small screens. Add an interchange placeholder to the **content area** of **media.html**

	    <!-- content area -->
	    <div data-interchange="[https://gist.githubusercontent.com/EdCharbeneau/5dc3f64f14511dd41f21/raw/481256a3dc469b6d6a86a6425e74348af8f8f22a/_media.html, (small)]"></div>
	    <!-- /content area -->
- Open index.html in the browser and resize the browser, **REFRESH** after resizing to observe how the page is rendered at different sizes. *The page must be refreshed because interchange is triggered on page load.*