# **PHP Syntax Guide**  

This guide will explain some basic PHP syntax, and show examples of them.  

**Comments**  
Comments are used to make notes within your written code, that will be ignored when the code is being rendered by the browser/server.  
To add a comment use a double forward slash at the beginning of the line of code  
	// *comment/code here*  
	
**PHP Variables**  
Variables are used to store information.  
To declare a variable in PHP use the $ followed by your desired variable name  
	$*variable name*  
	
**PHP Echo / PHP Print**  
PHP echo and PHP print are both used to display the output in the browser, with a couple small differences:

Echo can take multiple parameters, and has no return value. Echo is faster than print.  
	<?php  
	$variable = "You can include variables in echo statements";  
	echo $variable;  
	echo " *string* ";  
	echo "<p> you can include HTML in an echo statement.</p>";  
	?>  

Print can only accept one argument, and has a return value of 1, allowing you to use it in expressions.  
	<?php  
	