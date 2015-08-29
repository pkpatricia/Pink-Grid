#PINK MAGIC/PINK GRID/PINK ROW
###Sass Grid Mixin Solutions
*Version 0.1*

Inclue this file to easily generate widths/padding for items and build items which conform to a grid for your site.
Or, use Magic Grid to create a fully responsive equal-sized grid instantly!
No more dealing with annoying floats, rows, and clears! Using the magic of display: inline-block

Use `@include pinkgrid` to generate widths and padding for your own class-based grid system ( 1col, 2col, full, etc. ) or simply add directly to items.
Use`@include pinkrow` to remove the outer padding 
Use with media queries for even more responsive goodness!

`@include pinkgrid( $align, $totalcols, $colspan, $padtop, $padside )`

* $defaultcols:	12 	- Change this value to set the global number of columns in your grid system
* $defaultpad:	1%	Change this value to set the global padding percentage in your grid system
* $align:		Vertical-align property 										- Defaults to Top
* $totalcols: 	Number of columns in your grid ( ex: 12 ) 						- Defaults to $defaultcols
* $colspan: 	Number of columns your item spans ( ex: 3 / 12 ) 				- Defaults to $defaultcols (100% width)
* $padside:		Padding left/right of each item. 								- Defaults to $defaultpad
* $padtop:		Padding above/below around each item. 							- Defaults to 0


`@include pinkrow( $rowitems, $skipitems )`

* $rowitems:	Number of items per row ( ex. 4 )					 							- Defaults to 1
* $skipitems:	Create alternating row layouts (only numbers evenly divisible into $rowitems)	- Defaults to 0

`@include pinkmagic( $rowitems, $padtop, $padside, $align, $altrow )`

* $magicrow: 	4; 			- Change this value to set the global default number of items per row
* $magictop: 	10px;		- Change this value to set the global default of top padding
* $magicside:	2%;			- Change this value to set the global default of side padding
* $magicalign:	top;		- Change this value to set the global default of vertical-align

* $tiny-bp: 	300px;		- Change this value to set your tiny breakpoint
* $sm-bp:		480px;		- Change this value to set your small breakpoint
* $med-bp:		720px;		- Change this value to set your medium breakpoint
* $lg-bp:		980px;		- Change this value to set your large breakpoint
* $xl-bp:		1200px;		- Change this value to set your x-large breakpoint

* $rowitems:	Number of items per row ( ex. 4 )												- Defaults to 1
* $padside:		If $autopad is false, it will use this value to manually add side padding. 		- Defaults to $defaultpad
* $padtop:		Percentage padding above/below around each item. 								- Defaults to $magictop
* $align 		Vertical-align property 														- Defaults to Top
* $altrow:		Create alternating row layouts (only numbers evenly divisible into $rowitems)	- Defaults to 0


For example: 

`@include pinkgrid( $colspan: 3 )` will generate an object that spans 3 out of 12 columns ( 25% ) with 1% padding

`@include pinkgrid( $totalcols: 6, $colspan: 3 )` will generate an object that spans 3 out of 6 ( 50% ) columns with 1% padding

`@include pinkgrid( $colspan: 3 ) @include pinkrow( $rowitems: 4 )` will generate an object that spans 3 out of 12 columns ( 25% ) but will remove the outside padding of the first and last item in each row, based on having 4 items per row

`@include pinkmagic( $rowitems: 8 )` will generate a fully responsive grid for all items with that class, with 8 items across, complete with breakpoints

*Check out the example html/scss files for more ideas!*

Here's a [live version of the site](http://michelleschulp.pink/pink-grid) to see examples.

###Example screenshots:
![Screenshot](screenshot.png)
![Screenshot2](screenshot2.png)



