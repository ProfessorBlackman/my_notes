function, sum_list  
   if list has a single element  
     return that single element  
   otherwise...  
     add first element to value of sum_list called with every element minus the first

CALL STACK EMPTY  
___________________  
  
Our first function call...  
sum_list([5, 6, 7])  
  
CALL STACK CONTAINS  
___________________  
sum_list([5, 6, 7])  
with the execution context of a list being [5, 6, 7]  
___________________  
  
Base case, a list of one element not met.  
We invoke sum_list with the list of [6, 7]...  
  
CALL STACK CONTAINS  
___________________  
sum_list([6, 7])  
with the execution context of a list being [6, 7]  
___________________  
sum_list([5, 6, 7])  
with the execution context of a list being [5, 6, 7]  
___________________  
  
Base case, a list of one element not met.  
We invoke sum_list with the list of [7]...  
  
CALL STACK CONTAINS  
___________________  
sum_list([7])  
with the execution context of a list being [7]  
___________________  
sum_list([6, 7])  
with the execution context of a list being [6, 7]  
___________________  
sum_list([5, 6, 7])  
with the execution context of a list being [5, 6, 7]  
___________________  
  
We've reached our base case! List is one element.  
We return that one element.  
This return value does two things:  
  
1) "pops" sum_list([7]) from CALL STACK.  
2) provides a return value for sum_list([6, 7])  
  
----------------  
CALL STACK CONTAINS  
___________________  
sum_list([6, 7])  
with the execution context of a list being [6, 7]  
RETURN VALUE = 7  
___________________  
sum_list([5, 6, 7])  
with the execution context of a list being [5, 6, 7]  
___________________  
  
sum_list([6, 7]) waits for the return value of sum_list([7]), which it just received.  
  
sum_list([6, 7]) has resolved and "popped" from the call stack...  
  
  
----------------  
CALL STACK contains  
___________________  
sum_list([5, 6, 7])  
with the execution context of a list being [5, 6, 7]  
RETURN VALUE = 6 + 7  
___________________  
  
sum_list([5, 6, 7]) waits for the return value of sum_list([6, 7]), which it just received.  
sum_list([5, 6, 7]) has resolved and "popped" from the call stack.  
  
  
----------------  
CALL STACK is empty  
___________________  
RETURN VALUE = (5 + 6 + 7) = 18