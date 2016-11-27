
<!DOCTYPE html>
<html>
  <head>
      <title>javascript</title>
      <link type="text/css" rel="stylesheet" href="styles/bootstrap.min.css">
      <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css" integrity="sha384-1q8mTJOASx8j1Au+a5WDVnPi2lkFfwwEAa8hDDdjZlpLegxhjVME1fgjWPGmkzs7" crossorigin="anonymous">
      <script src="https://code.jquery.com/jquery-1.10.2.js"></script>
      <!--script src="scripts/work-scripts.js" type="text/javascript"></script-->
      <style>
          body {
              background-color: lightgreen;
              background:url(images/Capture.PNG) no-repeat 0px 0px;
	          background-size:cover;
	          width:100%;
	          min-height:700px;
          }
          
          .btn-primary {
              background-color: forestgreen;
              padding: 5px;
          }
          .bg-info {
              background-color:  rgb(219, 242, 72);
          }
          li {
              list-style: none;
          }
          .right
          {
              float : right
          }
      </style>
      
<script>
    
function temperature() {
    
    var temp = prompt("Please enter the temperature in Fahrenheit");
    temp = parseInt(temp);
    alert ("the temperature in C is  " + (temp - 32)/1.8);
 }
     
function addTwo() {

var a=0;
var b=0;
var c=0;
a = prompt("What is the first number?");
b = prompt("What is the second number?");
c = parseInt(a)+parseInt(b);
while (isNaN(c)) {
   a = prompt("Only numbers may be entered. What is the first number?");
   b = prompt("Only numbers may be entered. What is the second number?");
   c = parseInt(a)+parseInt(b);
}
alert("the number is " + c);
}



function fiborecur(){
    var a=1;
    var b=0;
    var c=0;
    var aa=prompt("Please enter a number");
    num = parseInt(aa);
    while (num >= 0) {
       c = a;
       a = b + a;
       b = c;
       num--;
    }
   alert("The Fibo. for " + aa + "  is  " +b);
}


function factorial() {
var i = 1;
var c = 1;
var b = prompt("What is the number ?");
a = parseInt(b)  
if (a < 0) {
        alert (" The factorial for " + a + "  is  " + -1 ) ;
        return;
} else if (a == 0) {
        alert (" The factorial for " + a + "  is  " + 1 ) ;
        return;
    }
var tmp = a;
    while (a-- > 2) {
        tmp *= a;
    }
alert (" The factorial for " + a + " is " + tmp);  
}
    
function fizzbuzz(){
    var b = prompt("What is the number ?");
    var x = parseInt(b)
    for(var i = 1; i <= x; i++){
    if(i % 5 !== 0 && i % 3 === 0){
      document.write(i + "<span style='color:orange; font-weight:bold'>  fizz</span>" + "<br>");
      } else if(i % 5 === 0 && i % 3 !== 0){
      document.write(i + "<span style='color:red; font-weight:bold'>  buzz</span>" + "<br>");
      } else if(i % 5 === 0 && i % 5 === 0){
      document.write(i + " <span style='color:blue; font-weight:bold'> fizzbuzz</span>" + "<br>");
      } else {
      document.write("<span style='color:black'>"+i+"</span><br>");
     }
   }
}
    
 
function nubmberExchange() {
    
var a = 0;
var c = 0;
var hexa = 0;
var octa = 0;
var bin = 0;
a = prompt("What is the number?");
while (isNaN(a)) {
   a = prompt("Only numbers may be entered. What is the number?");
}
b = parseInt(a);   
hexa = b.toString(16);
octa = b.toString(8);
bin = b.toString(2);
alert( a + "  In decimal  " + hexa + " in Hexadecimal  " + octa +" in Octal  " + bin + "  in Binary");
    
}
 
function strToArray() {
                               
   
var string = "Hussein like javascript and Html ";
var array = [];


document.write ("The string is  " + string +"<br>");
array = string.split(" ");
for (var i=0; i<array.length; ++i) {
     document.write (array[i] + "<br>");                     
}
}
    
</script>
  </head>
    <body class="mainDiv">
        <div class="container-fluid">

             <div class="text-center btn-primary">
                  <h3 class="shadow">Javascript Exercises</h3><p class="makeinline">Here are Javascript Lessons I am learning in New Americans Code. I will add more functions as I learn them.</p>
             </div>
             <div>
                  <h4 class=" text-center btn-primary shadow">JAVASCRIPT FUNCTIONS </h4>
                 <ol>
                     <li >
                          <button class="btn bg-info" onclick="addTwo()"><b>Add two numbers</b></button>
                     </li>
                     <br/>
                     <li> 
                    
                         <button class="btn bg-info" onclick="fiborecur()"><b>Compute the Fibonacci Sequence With Recursion</b></button>
                     </li>
                     <br/>
                     <li>
                          <button class="btn bg-info" onclick="factorial()"><b>Compute the Factorial of Any Number</b></button>
                     </li>
                     <br/>
                     <li>
                         <div id="right" class="panel panel-heading panel-group panel-success" style="width : 270px">
                            <h2>JavaScript temperature conversion. Please choose a method. </h2>
                         <div class="panel-body">
                             <a href="temp1.html" target="_blank">
                             <button  class="btn bg-info"><b>with the one group button</b></button>
                             </a>
                         </div> 
                         <div class="panel-body">
                             <a href="temp2.html" target="_blank">
                             <button  class="btn bg-info"><b>with 2 group button</b></button>
                             </a>
                         </div>
                         <div class="panel-body">
                             <a href="temp-che.html" target="_blank">
                             <button  class="btn bg-info"><b>with checkbox</b></button>
                             </a>
                         </div>
                         <!--div class="panel-body">
                             <a href="temperature.html" target="_blank">
                             <button  class="btn bg-info"><b>with the select from menu</b></button>
                             </a> 
                         </div-->
                         </div>
                     </li>
                     <li>
                          <button class="btn bg-info" onclick="fizzbuzz()"><b>Fizzbuzz - Numbers Divisible By 3: Fizz; By 5: Buzz; By 3 and 5: FizzBuzz</b></button>
                     </li>
                     <br/>
                     <li>
                          <button class="btn bg-info" onclick="nubmberExchange()"><b>Change Decimal number to Hexadecimal and Octal and Binary number</b></button>
                     </li>
                     <br/>
                     
                     <br/>
                     <li>
                         <a href="change.html" target="_blank">
                         <button  class="btn bg-info"><b>What can Javascript change ?</b></button>
                         </a>
                     </li>
                     <br/>
                     <li>
                          <button class="btn bg-info" onclick="strToArray()"><b>Splite a text to word word</b></button>
                     </li>
                 </ol>                                              
             </div> 
        </div>
                                                                             
  </body>
</html>
