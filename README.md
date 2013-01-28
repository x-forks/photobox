photobox
========

A lightweight CSS3 image gallery that is pretty to look and and easy to use.

##[Demo page](http://dropthebit.com/demos/photobox/), [Blog post](http://dropthebit.com/500/photobox-css3-image-gallery-jquery-plugin/)

## benefits
* Both the script & CSS are ~9k each (minified script) and can get much less using gzip compression.
*    Uses silky-smooth, hardware accelerated, CSS3 transitions and animations (for better performance)
*   Pretty UI and easy UX
*   Built so everything could be changed directly from the CSS 
*   CSS3 pre-loader, tailored-made
*   The only image is a pre-loader animation for old IE. For the rest, no images at all!
*   Works also on IE8 and above, but clearly not as nice as on modern browsers
*   Uses event-delegation on all thumbnails clicks
*   Observes DOM changes (if images were added or removed) and adapt accordingly



## Funcionality

*    Images can be zoomed in and out with mousewheel and navigated using mousemove to move around
*    Bottom row of thumbnails, navigated by mouse movment
*    Shows the image's 'alt' or 'title' attribute text at the bottom
*    Indicate the index of the current viewed image in relation to the total, like so: (36/100)
*    Supports looping after first and last images
*    Auto-playing of images at a set interval (see "time" in Settings)
*    Supports keyboard keys for navigation and closing the gallery view
*    In case there was an error loading an image, a message is showen, which can be configured via CSS

## Basic use-case example:
    <div id='gallery'>
        <a href="http://www.somedomain.com/images/image1_large.jpg">
        	<img src="http://www.somedomain.com/images/image1_small.jpg" alt="photo1 title">
    	</a>
    	<a href="http://www.somedomain.com/images/image2_large.jpg">
    		<img src="http://www.somedomain.com/images/image2_small.jpg" alt="photo2 title">
    	</a>
    	<a href="http://www.somedomain.com/images/image3_large.jpg">
    		<img src="http://www.somedomain.com/images/image3_small.jpg" alt="photo3 title">
    	</a>
    	<a href="http://www.somedomain.com/images/image4_large.jpg">
    		<img src="http://www.somedomain.com/images/image4_small.jpg" alt="photo4 title">
    	</a>
    </div>
    ...
    ...
    ...
    <script>
        // applying photobox on a `gallery` element which has lots of links which thumbnails in them, and passing an options object as well:
    	$('#gallery').photobox('a',{ time:0 });
    </script>

## settings
**time** (default: 3000) minimum 1000ms allowed

    The time in miliseconds when autoplaying a gallery. Set as '0' to hide the autoplay button completely.

**autoplay** (default: false)

    should the gallery autoplay on start or not.

**loop** (Default: 'true')

    Loop back to last image before the first one and to the first image after last one.
    
**thumbs** (Default: 'true') 

    Show thumbs of all the images in the gallery at the bottom.
   
**counter** (Default: 'true')

    Show the current image index position relative to the whole. Example (3,11). 
   
**hideFlash** (Default: 'true')

    Hide flash instances when viewing an image in the gallery.

**keys.close** (Default: "27, 88, 67")

    Key codes which close the gallery.

**keys.prev** (Default: "37, 80")

    Key codes which change to the previous image.

**keys.next** (Default: "39, 78")

    Key codes which change to the next image.
