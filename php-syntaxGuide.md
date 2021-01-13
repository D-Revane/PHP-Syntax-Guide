# **PHP Syntax Guide**  

This guide will explain some basic PHP syntax, and show examples of them.  

## **Comments**  

Comments are used to make notes within your written code, that will be ignored when the code is being rendered by the browser/server.  
To add a comment use a double forward slash at the beginning of the line of code  

	<?php  
	
	// *comment/code here*  
	
	?>
	
## **PHP Variables**  

Variables are used to store information.  
To declare/call a variable in PHP use the $ followed by your desired variable name  

	<?php  
	
	$*variable name*  
	
	?>  
	
## **PHP Echo / PHP Print**  

PHP echo and PHP print are both used to display the output in the browser, with a couple small differences:

Echo can take multiple parameters, and has no return value. Echo is faster than print.  

	<?php  
	
	$variable = "You can include variables in echo statements";  
	
	echo $*variable*;  
	echo " *string* " . $*variable*;  
	echo "<p> you can include HTML in an echo statement.</p>";  
	
	?>  

Print can only accept one argument, and has a return value of 1, allowing you to use it in expressions.  

	<?php  
	
	$*variable* = "you can use a string, or a $*variable* in yoyr statement";  
	
	print "*string";  
	print $*variable*;
	
	?>  

## **PHP Data Types**    

PHP includes the following data types:  

### Integers  

Integers are any whole numbers, numbers without decimal points.  

	<?php  
	
	$*variable1* = 123; // decimal base number integer  
	
	$*variable2* = -123; // a negative number integer  
	
	$*variable3* = 0X1A; // a hexidecimal number integer  
	
	$*variable4* = 0123; // an octal number integer  
	
	?>  

### Strings  

Strings are sequences of characters, where every character is the same as a byte (including spaces).  
A string can hold up to 2GB of characters. To specify a string, enclose the characters between quotes (single or double).  

	<?php  
	
	$*variable* = "*string...*";  
	
	$*variable* = '*string...*';  
	
	?>  

### Floating Point Numbers  

Floating point numbers are numbers containing a decimal point, or fractional numbers.  
Also referred to as *floats*, *doubles*, or *real numbers*.  

	<?php  
	
	$*variable1* = 1.234;  
	
	$*variable2* = 10.2e3;  
	
	$*variable3*  = 4E-10;  
	
	>?  

### Booleans  


	