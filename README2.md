http://learnyouahaskell.com/chapters



Introduction 
Haskell is: Lazy evaluating,  and statcially typed 
Starting Out

True, False, 
|| , && , \= , ==


Calling functions 
"infix" functions * , to write expressions like x * 3
"prefix" functions  like succ (short for successor) to write expressions like succ 8
````
div 92 10 -- is equivlent to 
92 'div' 10  
`````



First functions
````
doubleMe x = x + x  
````
````
doubleUs x y = doubleMe x + doubleMe y   
````

````
doubleSmallNumber x = if x > 100  
                        then x  
                        else x*2   
````                        



Conditional logic 


