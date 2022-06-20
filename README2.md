http://learnyouahaskell.com/chapters



#Introduction 
###General Notes and Syntax 
Haskell is: Lazy evaluating,  and statcially typed 

True, False

|| , && , \= , ==

"let" keyword 


#### Calling functions 
"infix" functions * , to write expressions like x * 3
"prefix" functions  like succ (short for successor) to write expressions like succ 8
````
div 92 10 -- is equivlent to 
92 'div' 10  
`````



### First functions
Functions cannot have first letter caps

#### examples: 
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

 

### Conditional logic 



### Data Structures 
#### Lists
Homogenous, so list is typed uniformly 
Indexing starts at 0 


!! operator to extract at index. 
++ operator to append lists. Note though Haskell must walk through left array, left to right. 
: is instant! 

examples 
````
ghci> let lostNumbers = [4,8,15,16,23,42]     --create 

ghci> [9.4,33.2,96.2,11.2,23.25] !! 1    -- get 
33.2  

ghci> [1,2,3,4] ++ [9,10,11,12]     --  '++' to append 
[1,2,3,4,9,10,11,12]   

ghci> 5:[1,2,3,4,5]      -- ':' to append
[5,1,2,3,4,5]   
````

[1,2,3] is actually just syntactic sugar for 1:2:3:[]



