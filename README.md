shiny-responsive-slider
=======================

A modified version of the Genesis Responsive Slider. 
I've added an action hook so that HTML code can be added to the slider container. 

An action hook was placed right before the ending div#shiny-responsive-slider (#genesis-responsive-slider).

Action Hook:

     shiny_after_slider
     
Example Usage: 

/** Add an action to add a static text area with a link to the contact page. **/

add_action( 'shiny_after_slider', 'shiny_slider_static_text' );
function shiny_slider_static_text () {
  
	echo '<div id="static-slide-text"><div class="wrap"><div class="bk-wrap">';
	echo '<p class="slider-callout">';
	echo '<a href="/contact">Schedule Your<br/>Consultation Now&#33;</a>';
	echo '</p>';
	echo '</div><!-- end of .bk-wrap --></div><!-- end of .wrap --></div><!-- end of #static-slide-text -->';	
		
}
		     
