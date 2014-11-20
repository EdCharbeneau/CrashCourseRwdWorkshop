#Interchange

Interchange uses media queries to dynamically load responsive content that is appropriate for different users' browsers.

1. Open index.html for editing
2. Create a style sheet named **site.css**. This style sheet will be used to theme the site. To expedite the process, this file has already been created */begin/site.css*
3. Find **foundation.css** and on the next line add a reference to **site.css** 

	    <link rel="stylesheet" href="css/foundation.css" />
	    <link rel="stylesheet" href="css/site.css" />
4. Open index.html in the browser and resize the browser, observe how the page is rendered at different sizes.
5. Open **site.css** for editing
6. Add a media query to target medium and larger devices. See: http://foundation.zurb.com/docs/media-queries.html

		/* medium up */
		@media only screen and (min-width: 40.063em) {	}

7. Increase the top and bottom padding for sections and footer, only for medium and up.

		/* medium up */
		@media only screen and (min-width: 40.063em) {
		    body > section, footer {
		        padding-top: 40px;
		        padding-bottom: 40px;
		    }
		}
8. Correct the button elements so they are not full width on medium and up.

		/* medium up */
		@media only screen and (min-width: 40.063em) {
		    body > section, footer {
		        padding-top: 40px;
		        padding-bottom: 40px;
		    }
		    .button {
		        display: inline-block;
		    }
		}
9. Modify the twitter panel so it covers the entire width of the screen on small screens. Make sure the style is zeroed out on medium and up.

		.panel.twitter {
		    background-color: #31CBF2;
		    margin-left: -15px;
		    margin-right: -15px;
		}

		...

		/* medium up */
		@media only screen and (min-width: 40.063em) {
		    body > section, footer {
		        padding-top: 40px;
		        padding-bottom: 40px;
		    }
		    .button {
		        display: inline-block;
		    }
		    .panel.twitter {
		        margin: 0;
		    }
		}
