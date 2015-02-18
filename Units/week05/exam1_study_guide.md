##Exam 1 Study Guide

###Notes
* Not everything listed here may be on the exam
* You will be able to use notes and nitrous to test and verify things.
* You will be given the entire class time to answer the questions and will turn in the results on paper.  
* The exam will be posted online for you to access during the class period.

### Examples and things to consider
Be able to describe the different kinds of variables being used. Are they scaler? What are their data types?
```
<html>
 <body>
  <?php
    // Code sample 1
    $var_a = 'Fred';
    $var_b = "Barney";
    $var_c = 123;
    $var_d = 456;

    print 'Variable a is $var_a';
    echo "<br />";
    echo "Variable b is $var_b<br/>";
  ?>
</body>
</html>
```

How does this html relate to the PHP script below it?  Wat are the variables the PHP script should expect to recieve.
```
<html>
 <head>
  <title>Sample2 HTML Form</title>
 </head>
 <body bgcolor="lightblue">
  <font size="+1">
  <form action="e1sample2.php" method="POST">
   <p>
   please enter your name: <br />
   <input type="text" size=30 name="userName" />
   <br />
   please enter your phone number: <br />
   <input type="text" size=30 name="userPhone" />
   <br />
   <input type=submit value="submit" />
   </p>
  </form>
  </font>
 </body>
</html>
```

Be able to describe each line of the following PHP script.  What is an issue you may have with using extract over specifying which form elements to get data from?
```
<?php
  // This is the PHP script that processes the form: simple.html
  extract($_REQUEST);
  print 'Your name is: '. $userName .'<br />';
  print "Your phone number is: $userPhone<br />";
?>
```

Be able to understand the types of loops and how they work.
```
<html>
 <head>
  <title>Sample 3</title>
 </head>
 <body>
  <h2>Celsius to Farenheit Conversion</h2>
  <table>
  <tr><th>Celsius</th><th>Farenheit</th><tr>
  <?php
    $C = -50;
    while ($C < 100) {
      $F = ($C * 1.8) + 32;
      print "<tr><td>$C</td><td>$F</td>";
      if ($F == 32) {
        break;
      }
      $C += 5;
    }
  ?>
  </tr>
  </table>
  <table>
  <tr><th>Celsius</th><th>Farenheit</th><tr>
  <?php
    for ($C = -50; $C < 100; $C += 5) {
      $F = ($C * 1.8) + 32;
      print "<tr><td>$C</td><td>$F</td>";
    }
  ?>
  </tr>
  </table>
 </body>
</html>
```

What effect does the pre tag have on this code?
```
<html>
 <head><title>Sample 4</title></head>
 <body>
  <pre>
  <?php
    $str1 = "Dan";
    $str2 = "Daniel";
    $str3 = "new york";
    $str4 = "New York";
    
    if ($str1 == $str2) {
      print "\n'$str1' equals '$str2'\n";
    }
    else {
      print "\n'$str1' not equal to '$str2'\n";
    }
    if (strcmp($str1, $str2) == 0) {
      print "\n'$str1' equals '$str2'\n";
    }
    else {
      print "\n'$str1' not equal to '$str2'\n";
    }
    if (strcmp($str1, substr($str2, 0, 3)) == 0) {
      print "\n'$str1' equals '". substr($str2, 0, 3) ."' from '$str2'\n";
    }
    else {
      print "\n'$str1' not equal to '". substr($str2, 0, 3) ."' from '$str2'\n";
    }
    if (strcasecmp($str3, $str4) == 0) {
      print "\n'$str3' equals '$str4' (case-insensitive)\n";
    }
    else {
      print "\n'$str3' not equal to '$str4' (case-insensitive)\n";
    }
  ?>
  </pre>
 </body>
</html>
```

Be able to describe how the array and loop are working.
```
<html>
 <head><title>Sample 5</title>
 </head>
 <body>
  <?php
    $colors = 'red green orange blue';
    echo '$colors is a '. gettype($colors) .'<br />';
    $employee = array('Name' => 'Jon Doe',
                      'ID' => '23d4',
                      'Job Title'=> 'Designer',
                      'Department'=>'Web Development'
                     );
    $colors = explode(" ", $colors);
    echo 'After explode(): $colors is an '. gettype($colors) .'<br />';
    echo "<hr>";
    
    foreach ($colors as $value) {
      echo "$value <br />";
    }
    echo "<hr>";
    
    foreach ($employee as $key => $value) {
      echo "employee[$key] => $value<br />";
    }
  ?>
 </body>
</html>
```

Be able to explain these functions and how the affect the variables in the script.
```
<?php
  $friend = "Sam";
  $friend2 = who();
  echo 'My friends are: ', $friend, ' ', $friend2, '<br />';
  
  function who() {
    $friend = "Joe"; 
    return $friend;
  }
  
  $friend3 = who();
  print 'My friends are: '. $friend .' '. $friend3 .'<br />';
  
  
  function raise_sal() {
    global $salary;
    $salary *= 1.1;
  }
  
  $salary = 50000;
  raise_sal();
  echo 'Congratulations! Your new salary is: $'. $salary .'<br />';
?>
```

Be able to explain the two kinds of arrays and how to get data out of them.
```
<?php

$items = array("milk", "eggs", "cheese", "bacon");
	
$person = array("name"=>"joe blow", "email"=>"jblow@madisoncollege.edu", "id"=>1);
	
foreach($person as $attr=>$val) {
	printf("key: %s<br />value: %s<br /><hr />", $attr, $val);
}
	
$i = 0;
while($i < count($items)) {
	echo $items[$i];
	echo "<br />";
	$i++;
}
	
?>
```

Be able to describe the HTML form and it's PHP counter part, what variables are being passed, etc.

Html Form
```
<html>
 <head><title>Sample 8</title></head>
 <body>
  <form action="e1sample8.php" method="POST">
   <p>
   Enter your name:<br />
   <input type="text" size=50 name="userName" />
   </p><p>
   Enter your phone:<br />
   <input type="text" size=50 name="userPhone" />
   </p><p>
   Enter your email address:<br />
   <input type="text" size=50 name="userEmail" />
   </p><p>
   <input type="hidden" name="formName" value="sample8" />
   <input type="hidden" name="createDate" value="March 2008" />
   <input type=submit name="send" value="submit" />
   <input type=reset value="clear" />
  </form>
 </body>
</html>
```

PHP Processing script
```
<html>
 <head><title>Sample 8</title></head>
 <body>
  <?php
    if ((!empty($_GET)) ||
        (!isset($_POST['formName'])) ||
        ($_POST['formName'] != 'sample8')) {
      die("Bad input data source<br />");
    }
    $name = $_POST['userName'];
    $phone = $_POST['userPhone'];
    $email = $_POST['userEmail'];
  ?>
  <div align="center">
   <table>
    <tr><td>
    Welcome to PHP, <em><?php echo $name; ?>.</em>
    </td></tr><tr><td>
    Can I call you at <em><?php echo $phone; ?>? </em>
    </td></tr><tr><td>
    Is it OK to send you email at <em><?php echo $email; ?>?</em>
    </td></tr>
   </table>
  </div>
 </body>
</html>
```