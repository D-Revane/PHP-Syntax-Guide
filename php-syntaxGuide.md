# **PHP Syntax Guide**  

This guide will explain some basic PHP syntax, and show examples of them.  

## **Comments**  

Comments are used to make notes within your written code, that will be ignored when the code is being rendered by the browser/server.  
To add a comment use a double forward slash at the beginning of the line of code  

	<?php  
	
	// comment/code here  
	
	?>
	
## **PHP Variables**  

Variables are used to store information.  
To declare/call a variable in PHP use the $ followed by your desired variable name  

	<?php  
	
	$variable name  
	
	?>  
	
## **PHP Echo / PHP Print**  

PHP echo and PHP print are both used to display the output in the browser, with a couple small differences:

Echo can take multiple parameters, and has no return value. Echo is faster than print.  

	<?php  
	
	$variable = "You can include variables in echo statements";  
	
	echo $variable;  
	echo " string " . $variable;  
	echo "<p> you can include HTML in an echo statement.</p>";  
	
	?>  

Print can only accept one argument, and has a return value of 1, allowing you to use it in expressions.  

	<?php  
	
	$variable = "you can use a string, or a $*variable* in yoyr statement";  
	
	print "string";  
	print $variable;
	
	?>  

## **PHP Data Types**    

PHP includes the following data types:  

### Integers  

Integers are any whole numbers, numbers without decimal points.  

	<?php  
	
	$variable1 = 123; // decimal base number integer  
	
	$variable2 = -123; // a negative number integer  
	
	$variable3 = 0X1A; // a hexidecimal number integer  
	
	$variable4 = 0123; // an octal number integer  
	
	?>  

### Strings  

Strings are sequences of characters, where every character is the same as a byte (including spaces).  
A string can hold up to 2GB of characters. To specify a string, enclose the characters between quotes (single or double).  

	<?php  
	
	$variable = "string...";  
	
	$variable = 'string...';  
	
	?>  

### Floating Point Numbers  

Floating point numbers are numbers containing a decimal point, or fractional numbers.  
Also referred to as *floats*, *doubles*, or *real numbers*.  

	<?php  
	
	$variable1 = 1.234;  
	
	$variable2 = 10.2e3;  
	
	$variable3*  = 4E-10;  
	
	>?  

### Booleans  

Booleans are the base of digital logoc programming, returning either true(1) or false(0) values.  

	<>php  
	
	$variable = 7;  
	
	if($variable == 7) {  
	
	return true;  // returned value is true, also equal to 1    
	
	}
	
	else {  
	
	return false;  // returned value is false, also equal to 0    
	
	}  
	
	?>  

### Arrays  

Arrays are variables that hold more than one value at a time, as an indexed collection of values.  

	<?php  
	
	$variable1 = array("coding", "is", "fun");  
	
	$variable2 = array(7, 12, 40, 42);  
	
	?>  

### Objects  

Objects are data types that allow for the storing of information, and how to process that data. Every object has properties and methods corrisponding to it's parent class.  

	<?php  
	
	// define class  
	
	class example {  
	
	  // properties  
	
	public $str = "Hello world";  
	
	  // methods  
	
	function show_greeting() {  
	
	return $this->str;  
	
	}}  
	
	// create object from class  
	
	$variable = new example;  
	
	?>  

### NULL    

NULL is a special value that represents empty variables. A variable type NULL is a variable without any data. NULL is the only possible value of type NULL.  

	<?php  
	
	$variable = NULL;  
	
	?>  

### Resources  

A resource is a special variable holding a reference to an external resource.  

	<?php  
	
	// open a file for reading  
	
	$handle = fopen("note.txt", "r");  
	
	?>  

## **Constants**  

The value of a constant can not be changed during the execution of the code. To define a constant use the define() method, giving the name of the constant as the first argument, and the value of the constant as the second argument. Unlike variables, constants do not require the $, and use all caps.  

	<?php  
	
	define('CONSTANT1', "Value of the constant");  
	
	?>  

## **Operators**  

Operators are symbols that tell the processor to perform certain actions. There are several different ways to use operators, such as:  

### Arithmatic Operators  

Used to perform common arithmatical operations such as addition, subtraction, multiplication, division, and modulous.  

	<?php  
	
	$x + $y;  // add x to y  
	
	$x - $y;  // subtract y from x  
	
	$x * $y;  // multiply x by y  
	
	$x / $y;  // divide x by y  
	
	$x % $y;  // remainder of x divided by y (modulous)  
	
	?>  

### Assignment Operators  

Used to assign values to variables  

	<?php  
	
	$variable1 = "This is the variables value";  // assign this string to variable 
	$variable2 = 7;  // assign value of 7 to variable  
	
	$x = 10;  
	$y = 20;  
	$x += 5;  // add 5 to 10 and assign value to x  
	$y *= 2;  // multiply 20 by 2 and assign value to y  
	
	?>  

### Comparison Operators  

Used to compare two values in a Boolean fashion. Returns true(1) or false(0).  

	<?php  
	
	$x == $y;  // true if x is equal to y  
	
	$x === $y;  // true if x is identical to y in both value, and type  
	
	$x != $y;  // true if x does not equal y  
	
	$x > $y;  // true if x is greater than y  
	
	$x <= $y;  // true if x is less than or equal to y  
	
	?>  

### Incrementing and Decrementing Operators  

Used to increment/Decrement a variables value. The increment/decrement can be executed before or after returning the value of the variable.   

	<?php  
	
	++$x;  // increment x by one, then return value  
	
	$y--;  // return value of y, then decrease by 1  
	
	?>  

### Logical Operators  

Typically used to combine conditional statements using *and*(&&), *or*(||), and *not*(!).  

	<?php  
	
	if($variable1 = 7) && ($variable2 = "test") {  
	return true;  // only if variable1 equals 7, AND variable2 equals test     
	}  
	else {  
	return false  
	}  
	
	while($variable3 = 1) || ($variable4 = "test") {  
	function myFunction() {  
	do this  // perform this action while variable3 equals 1, OR variable4 equals test  
	}}  
	
	?>  

### String Operators  

Used to concatenate strings with other strings, variables, or elements.  

	<?php  
	
	$variable1 = "This is a string";  
	$variable2 = "...and another one";  
	
	echo "Use the . to concate strings" . "<br>" . $variable1 . variable2;  
	
	?>  

### Array Operators  

Used to compare compare (returning Boolean true(1) or false(0)), or join arrays.  

	<?php  
	
	$variable1 = array("dog", "cat", "bird", "fish");  
	$variable2 = array("puppy", "kitten", "snake");  
	
	$variable1 + $variable2;  // union of variable1 and variable2  
	
	var_dump($variable1 == $variable2);  // returns Boolean false(0)  
	
	var_dump($variable1 != $variable2);  // returns Boolean true(1)  
	
	?>  

## **Functions**  

Fuctions are self-contained blocks of code that perform a specific task. PHP has a huge selection of built in functions that you can call within your scripts, or you can define your own functions to be called within your scripts.  

	<?php  
	
	$variable1 = "Hello world";  
	
	print_r($variable1);  // use built-in print_r function to display the value of variable1  
	
	function myFunction() {   // declare user-defined function called myFunction  
	$variable2 = "Functions are fun! ";  
	$variable3 = "They really are..";  
	echo $variable2 . $variable3;  
	}  
	
	myFunction();  // returns "Functions are fun! They really are.."  
	
	?>  

## **If, Else, and Elsif**  

Used for conditional statements. Conditional execution of one or more statements is the most important feature of any programming language. The code is only executed when the conditions are met, if not the processor moves on to the next step in the execution.  

	<?php  
	
	$variable1 = "password";  
	
	if($variable1 == true) {  
	execute this code  // if password is true do this  
	}  
	else {  
	do this  // if password is not true do this  
	}  
	
	if($variable2 < 10) {  
	do this  //  do this if variable2 is less than 10  
	}  
	elseif($variable2 < 20) {  
	do this instead   // do this if variable2 is 10 or greater and less than 20  
	}  
	else {  
	do this for everything else  //  do this if variable2 is 20 or greater  
	}  
	
	?>  

## **Loops**  

PHP supports four types of loops.  

### While Loop  

Loops through a block of code as long as the the condition specified in the while statement evaluates to true(1). The condition is evaluated at the beginning of each loop itteration.   

	<?php  
	
	while(condition) {  
	code to be executed  // keep looping through this code as long as condition is met  
	}  
	
	?>  

### Do..While Loop  

A varient of the while loop, thast evaluates the condition at the end of each loop itteration. The block of code is executed once, then the condition is re-evaluated, if true the code is executed again.  

	<?php  
	
	do {  
	code to be executed  
	}  
	
	while(condition);  
	
	?>  

### For Loop  

Typically used to execute a block of code for a certain number of times. For loops take three parameters:  
- initialization  
- condition  
-increment/decrement    

	<?php  
	
	for($x = 1; $x <= 10; $x++) {  
	echo $x;  // display value of x for each value from 1-10  
	}  
	
	// x is initialized as 1  
	// x can not be reach greater than 10  
	// increment x by 1 and return value  
	
	?>  

### Foreach Loop  

Used to iterate over arrays.  

	<?php  
	
	$variable1 = array("Finally", "Almost", "Done")  
	
	foreach($variable1 as $value) {  
	echo $value . "<br>";  // display each of the values in variable1 with line breaks  
	}  
	
	?>  



	
	
	
	
	


	
	
	