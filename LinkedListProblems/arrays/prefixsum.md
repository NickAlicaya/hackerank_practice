Nowadays, especially in the field of competitive programming, the utility of computing prefix sum is quite popular and features in many problems. Hence, having a one-liner solution to it would possess a great help. Let’s discuss certain way in which this problem can be solved.

Method #1: Using list comprehension + sum() + list slicing

This problem can be solved using the combination of above two functions in which we use list comprehension to extend logic to each element, sum function to get the sum along, slicing is used to get sum till the particular index.

filter_none
edit
play_arrow

brightness_4
# Python3 code to demonstrate 
# prefix sum list 
# using list comprehension + sum() + list slicing  
  
# initializing list 
test_list = [3, 4, 1, 7, 9, 1] 
  
# printing original list 
print("The original list : " + str(test_list)) 
  
# using list comprehension + sum() + list slicing 
# prefix sum list 
res = [sum(test_list[ : i + 1]) for i in range(len(test_list))] 
  
# print result 
print("The prefix sum list is : " + str(res)) 
Output :


The original list : [3, 4, 1, 7, 9, 1]
The prefix sum list is : [3, 7, 8, 15, 24, 25]