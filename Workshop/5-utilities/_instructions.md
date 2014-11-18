#Solving problems with utility classes

##Flex video and embedded content
1. Open index.html for editing
- In the **media** section, add a new row.


	    <section id="media">
	        <div class="row">
	
			</div>
		</section>
- Inside the row create three elements that will be:
	- Full width on a small device
	- 6 units width on a medium device
	- 4 units width on a large device

            <div class="small-12 medium-6 large-4 columns">
				<!-- embedded content -->
			</div>
            <div class="small-12 medium-6 large-4 columns">
				<!-- embedded content -->
			</div>
            <div class="small-12 medium-6 large-4 columns">
				<!-- embedded content -->
			</div>
- Add a embedded video to each element.

            <div class="small-12 medium-6 large-4 columns">             
                    <iframe width="1280" height="750" src="http://www.youtube.com/embed/fDSGh8i4hcs" frameborder="0" allowfullscreen></iframe>
            </div>
            <div class="small-12 medium-6 large-4 columns">
                    <iframe width="1280" height="750" src="http://www.youtube.com/embed/BbYnzyvl4Y4" frameborder="0" allowfullscreen></iframe>
            </div>
            <div class="small-12 medium-6 large-4 columns">
                    <iframe width="1280" height="750" src="http://www.youtube.com/embed/YDNmyyrEZho" frameborder="0" allowfullscreen></iframe>
            </div>
- Open index.html in the browser and resize the browser to see the effect. The embedded content doesn't obey the grid and breaks out of their containers.

- To solve this problem wrap each `<iframe>` with the `flex-video` utility class.

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
            <div class="small-12 medium-6 large-4 columns">
                <div class="flex-video">
                    <iframe width="1280" height="750" src="http://www.youtube.com/embed/YDNmyyrEZho" frameborder="0" allowfullscreen></iframe>
                </div>
            </div>

- Open index.html in the browser and resize the browser to see the effect. The embedded content now works as intended.

##Visibility classes

1. In the media section, add visibility classes to control the number of videos shown for each screen size. One for small, two for medium, and all three for large:
	- On the first element, do nothing
	- On the second element, replace `small-12` with `show-for-medium-up`
	- On the third element, replace `small-12` with `show-for-large-up`

            <div class="small-12 medium-6 large-4 columns">
                <div class="flex-video">
                    <iframe width="1280" height="750" src="http://www.youtube.com/embed/fDSGh8i4hcs" frameborder="0" allowfullscreen></iframe>
                </div>
            </div>
            <div class="show-for-medium-up medium-6 large-4 columns">
                <div class="flex-video">
                    <iframe width="1280" height="750" src="http://www.youtube.com/embed/BbYnzyvl4Y4" frameborder="0" allowfullscreen></iframe>
                </div>
            </div>
            <div class="show-for-large-up medium-6 large-4 columns">
                <div class="flex-video">
                    <iframe width="1280" height="750" src="http://www.youtube.com/embed/YDNmyyrEZho" frameborder="0" allowfullscreen></iframe>
                </div>
            </div>

- Since the user has to scroll much further on a small device, add a button to navigate back to the top of the page. After the last element, add the following markup:
	- Create element that is only visible to small screens
	- Inside that element add a paragraph with the text centered
	- Give the paragraph a button to navigate to the top of the page
	- Expand the button to cover the full width of its container

            <div class="small-12 columns show-for-small-only">
                <p class="text-center"><a href="#top" class="secondary button expand">top</a></p>
            </div> 

- Open index.html in the browser and resize the browser to see the effect.

