
Free for personal and commercial use under the JUST INFORM ME lincese.


PS: Not sure how to get that contact form working? Give formspree.io a try (it's awesome).


Instructions:

	Overview:

		Being a single pager, aside from a main page <header> and <footer>, it's pretty much just 
		a stack of "main" <section> elements that follow the same basic pattern:

			<section id="foobar" class="main">
				<div class="content container">
					<header>
						<h2>Foobar</h2>
					</header>
					...
				</div>
			</section>

		The section can then be assigned a style class to determine its basic
		look (and, in some cases, its behavior):

			style1
				Centered content with an oversized <h2>. Works best when
				paired with a background image or color.

			style2 left
				Content in a box, anchored to the left side of the window. Works
				best when paired with a background image or color. If you have
				"useSectionTransitions" turned on in your settings, the box will
				slide into view from the left.

			style2 right
				Content in a box, anchored to the right side of the window. Works
				best when paired with a background image or color. If you have
				"useSectionTransitions" turned on in your settings, the box will
				slide into view from the right.

			style3 primary
				Used for generic content. Set against the primary background
				color (default is white).

			style3 secondary
				Used for generic content. Set against the secondary background
				color (default is a light gray).

		Oh, and there are a few (well, two) optional modifier classes you can
		tack on for additional effects:

			dark
				Flips the content's color scheme so it shows up better
				against darker background images and colors.

			fullscreen
				Makes the section fill the entire window (only if "useFullScreen"
				is enabled in your settings).


	Lightbox Gallery:

 		The actual gallery function is powered by my Poptrox plugin. For info on
 		how that works, go here: github.com/ajlkn/jquery.poptrox

		Rows:

		 	The structure of the gallery is a skel grid. Each row looks like this:

			 	<div class="row flush images">
			 		<div class="6u">...<div>
			 		<div class="6u">...<div>
			 	</div>

			The "Xu" class indicates the width of the cell (in this case, both are 6).
			You can use any number of cells and any combination of widths provided their
			combined widths add up to exactly 12. So, if you needed, say, three images
			in a row, you can do something like this:

			 	<div class="row flush images">
			 		<div class="4u">...<div>
			 		<div class="4u">...<div>
			 		<div class="4u">...<div>
			 	</div>

			You can also use a "-Xu" class to "nudge" a cell over by that much, which
			comes in handy if you need to place just one image on a row and you want
			to center it:

			 	<div class="row flush images">
			 		<div class="6u -3u">...<div>
			 	</div>

			Which translates to "make this 6 wide and nudge it over to the right by
			another 3".

		Images:

			Each image (the '...' bit in the above examples) should look like this:

				<a href="path/to/fullsize.jpg" class="image fit from-(direction)">
					<img src="path/to/thumbnail.jpg" title="This is the image caption." alt="" /></a>
				</div>

			The "from-(direction)" class indicates the direction from which the image should
			slide into view, and can be any of the following:

				from-left
				from-right
				from-bottom
				from-left

			You can also just remove the "from-(direction)" class if you don't want that particular
			image to slide into view (in which case it'll simply fade in).


	Contact Form:

		To get this working, place a script on your server to receive the form data, then
		point the "action" attribute to it (eg. action="http://mydomain.tld/mail.php").
		More on how it all works here: 1stwebdesigner.com/tutorials/custom-php-contact-forms


    Icons:

     	Powered by Font Awesome. Go here for a full listing of all the icons you can use:
     	fortawesome.github.io/Font-Awesome/cheatsheet


	Other Stuff:

		- If you don't like the way images are tinted, either change "images/overlay.png"
		  to something else, or remove all references to it from css/style.css.

		- If you plan to keep support for IE8 (what little there is), don't forget to update
		  css/ie/ie8.css as you change other stuff.


Credits:


	Icons:
		Font Awesome (fortawesome.github.com/Font-Awesome)

	Other:
		jQuery (jquery.com)
		html5shiv.js (@afarkas @jdalton @jon_neal @rem)
		CSS3 PIE (css3pie.com)
		background-size polyfill (github.com/louisremi)
		Respond.js (j.mp/respondjs)
		jquery.poptrox (@ajlkn)
		jquery.scrolly (@ajlkn)
		jquery.scrollgress (@ajlkn)
		Skel (skel.io)
