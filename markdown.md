

CLOSURE:
-------------------------------------------------------------------------------------------------------------------------
      Closure is an object which has memory of the function and its lexical environment, in which it is created.
      
Closure have an access to:
-------------------------------------------------------------------------------------------------------------------------
Its own local variables.
Outer function's variables & parameters.
Global variables.

For Example,
              var a             /*Global Variables*/ 
              
              Func1(x,y){
                  var z         /*Outer Function Variables*/
                  
                  Func2(){      /*Inner Function have access to all three type of variables and parameters as well.*/
                   var b        /*Local Variables*/
                   
                  }
                }
                
Consider an example :
--------------------------------------------------------------------------------------------------------------------------     
 
 function add(a,b,c){
    
    var x= (a+b+c)
    
    return function avg(){
        var y=(x/3)
         console.log("average of marks:"+y)
        
        return function percent(){
          console.log("Percentage:"+y+"%")
        
         }
    }
}
 
 add(75,83,90)

 
Note:

1) The add() function return its inner function avg() and then to percent().By returning reference to an inner functions ,
   closure is created.
2) When avg() and percent() functions are called ,closure is created.


A closure is created when an inner function is made accessible from outside of the function that created it. This typically occurs
when an outer function returns an inner function.  When this happens, the inner function maintains a reference to the environment 
in which it was created.  This means that it remembers all of the variables (and their values) that were in scope at the time.




Reference taken from:
   > https://javascriptweblog.wordpress.com/2010/10/25/understanding-javascript-closures/
   >http://javascript.info/tutorial/closures
   >http://bonsaiden.github.io/JavaScript-Garden/
   >Video-https://www.youtube.com/watch?v=oWSQ4mWNFPU
   
   
   