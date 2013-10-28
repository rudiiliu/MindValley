MindValley
==========
<?php
/*
Plugin name: WordPress Most Popular
Plugin URI: http://testing.com
Description: A plugin that checks for most popular posts.
Author: Calvin
Author URI: http://calvin698.com
Version: 1.0
*/

/****
Global
****/

function wp_most_popular_page(){
	ob_start();
?>

	<h1> List of most popular sites </h1>
	
<?php
	echo ob_get_clean();

}

//admin tab

function wp_most_popular(){

	add_options_page('wp most popular','Most Popular','manage_options','wpmostpopular','wp_most_popular_page');

}
add_action('admin_menu','wp_most_popular');

?>
