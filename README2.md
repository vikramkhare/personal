http://learnyouahaskell.com/chapters



#Introduction 
##General Notes and Syntax 
Haskell is: Lazy evaluating,  and statcially typed 

True, False

|| , && , \= , ==

"let" keyword 

Beware underlying floating points, eg 
````
ghci> [0.1, 0.3 .. 1]  
[0.1,0.3,0.5,0.7,0.8999999999999999,1.0999999999999999]  
````


###  functions 
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



## Data Structures 
### Lists
Homogenous, so list is typed uniformly 
Indexing starts at 0 


!! operator to extract at index. 
++ operator to append lists. Note though Haskell must walk through left array, left to right. 
: is instant! 



### Tuples 
Formed with () 
[(1,2),(8,11),(4,5)] 

A list of tuples, would enforce that length of tuple !


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

<, <=, > and >=  to compare based on lexigraphical order

functions:

head mylist     first element only 
tail myList     list without first element 
last myList     only the last item 
init myList     list without last element 

error message when called on empty list 

length myList     returns length 
null myList
reverseMyList
take MyList n     returns list of first n elements 
drop myList n     returns lsit of last n elemetns 
maximum myList
minimum myList
sum myList 
product myList 
n 'elem' myList   returns if n is an element of the list 





Quickly form ranges, like other interpreted languages. 
````
ghci> [1..20]  
[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20]  
ghci> ['a'..'z']  
"abcdefghijklmnopqrstuvwxyz"  
ghci> ['K'..'Z']  
"KLMNOPQRSTUVWXYZ"   

ghci> [2,4..20]  
[2,4,6,8,10,12,14,16,18,20]  
ghci> [3,6..20]  
[3,6,9,12,15,18]   
````

#### List Comprehension 

Looks like set notation in mathematics 
````
ghci> [x*2 | x <- [1..10]]  
[2,4,6,8,10,12,14,16,18,20]  
````
Stack conditons, called "filtering": 
````
ghci> [x*2 | x <- [1..10], x*2 >= 12]  
[12,14,16,18,20]  

-- If we wanted all numbers from 10 to 20 that are not 13, 15 or 19, we'd do: 
ghci> [ x | x <- [10..20], x /= 13, x /= 15, x /= 19]  
[10,11,12,14,16,17,18,20]  
````


Advanced
````
length' xs = sum [1 | _ <- xs]  
````
Calls sum on the list, with each element replaced by 1. 






TODO : Advanced 






