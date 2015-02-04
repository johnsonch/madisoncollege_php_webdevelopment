#Exercise 1

Copy and paste the following content in to your www/labs/week03 folder as a new file called myform.html.

```
<html>
 <head>
  <title>My Form</title>
 </head>
 <body>
  <h2 align="center">My Form</h2>
  <form name="myform" method="post" action="myscript.php" enctype="multipart/form-data">
  <table width="400" border="1" align="center" cellpadding="5" cellspacing="0" bgcolor="#CCCCCC">
    <tr> 
     <td width="47%">Full Name</td>
     <td colspan="2"> 
      <input type="text" name="name" size="25" maxlength="25">
     </td>
    </tr>
    <tr> 
     <td width="47%" height="57">Address</td>
     <td height="17" colspan="2"> 
      <textarea name="address" cols="26" rows="4"></textarea>
     </td>
    </tr>
    <tr> 
     <td width="47%">Email</td>
     <td height="2" colspan="2"> 
      <input type="text" name="email" size="25" maxlength="50">
     </td>
    </tr>
    <tr>
     <td width="47%">DoB</td>
     <td height="2" > 
      <select name=birth_month>
       <option selected value=1>January 
       <option value=2>February 
       <option value=3>March 
       <option value=4>April 
       <option value=5>May 
       <option value=6>June 
       <option value=7>July 
       <option value=8>August 
       <option value=9>September 
       <option value=10>October 
       <option value=11>November 
       <option value=12>December</option>
      </select>
      <select name=birth_day>
       <option selected value=1>01 
       <option value=2>02 
       <option value=3>03 
       <option value=4>04 
       <option value=5>05 
       <option value=6>06 
       <option value=7>07 
       <option value=8>08 
       <option value=9>09 
       <option value=10>10 
       <option value=11>11 
       <option value=12>12 
       <option value=13>13 
       <option value=14>14 
       <option value=15>15 
       <option value=16>16 
       <option value=17>17 
       <option value=18>18 
       <option value=19>19 
       <option value=20>20 
       <option value=21>21 
       <option value=22>22 
       <option value=23>23 
       <option value=24>24 
       <option value=25>25 
       <option value=26>26 
       <option value=27>27 
       <option value=28>28 
       <option value=29>29 
       <option value=30>30 
       <option value=31>31</option>
      </select>
      <input maxlength=4 name=birth_year size=4>
      (yyyy) 
     </td>
    </tr>
    <tr> 
     <td width="47%"> 
      Gender
     </td>
     <td>
      <table border=0>
        <tr>
         <td height="2" width="26%"> 
          <input type="radio" name="gender" value="Male">
           Male 
         </td>
         <td height="2" width="27%"> 
          <input type="radio" name="gender" value="Female">
           Female
         </td>
        </tr>
       </table>
      </td>
     </tr>
     <tr> 
      <td width="47%"> 
       Please choose Topics of Interest
      </td>
      <td height="2" > 
       <table width="100%" border="0">
        <tr> 
         <td> 
          <input type="checkbox" name="fiction" value="1">
          Fiction
         </td>
         <td> 
          <input type="checkbox" name="horror" value="1">
          Horror
         </td>
        </tr>
        <tr> 
         <td> 
          <input type="checkbox" name="action" value="1">
          Action 
         </td>
         <td> 
          <input type="checkbox" name="comedy" value="1">
          Comedy
         </td>
        </tr><tr>
        <td>&nbsp;</td>
        </tr>
       </table>
      </td>
     </tr>
     <tr> 
      <td colspan="3"> 
       <input type="submit" name="Submit" value="Submit">
      </td>
     </tr>
    </table>
  </form>
 </body>
</html>
```
#Exercise 2

- Create a script named myscript.php and save it into your labs/week03 directory.
- Add PHP variables to hold the values of the fields from the HTML form.
- PHP uses the $_POST[ ] array to hold form field values after the form is posted.

For example, if there is a form field called "name", your variable assignment statement will look like:

```
  $name = $_POST['name'];
```

Add PHP code blocks embedded in HTML to print the descriptions and values of all fields entered in the myform.html HTML form. If a form field is empty, print a "no value submitted" message instead of the field value.

Test your code and show it to your instructor.