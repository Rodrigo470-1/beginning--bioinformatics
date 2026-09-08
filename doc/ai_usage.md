# AI Use Log
- Tool/model & version:
- What I asked for:
- Snippet of prompt(s):
- What I changed before committing:
- How I verified correctness (tests, sample data)



I originally proposed this code to solve problem 2 : 
array = ['HumptyDumptysatonawallHumptyDumptyhadagreatfallAlltheKingshorsesandalltheKingsmenCouldntputHumptyDumptyinhisplaceagain.']
c = array [22:28] + array [97:103]
print (c)

Which then later I asked gemini to help me understand what was wrong and add this lines of code lines : 
string_to_slice = array[0]
c = string_to_slice[22:28] + ' ' + string_to_slice[97:103]
explaining that it was trying to slice the list, but not the string itself.


3rd 
array = [] # Corrected: Initialized as an empty list
for i in range (10000):
  if a % 3 == 0: # Check if 'a' is divisible by 3
    array.append(a)
  a += 1 # Increment 'a' for the next iteration, regardless of if condition

  if b % 3 == 0: # Check if 'b' is divisible by 3
    array.append(b)
  b += 1 # Increment 'b' for the next iteration, regardless of if condition

number = sum(array)
print (number)
print (array)

AI gave me this solution guessing what my intend with the code was
if a % 3 == 0: # Check if 'a' is divisible by 3
    array.append(a)
  a += 1 # Increment 'a' for the next iteration, regardless of if condition

  if b % 3 == 0: # Check if 'b' is divisible by 3
    array.append(b)
  b += 1 # Increment 'b' for the next iteration, regardless of if condition
Original
  if a/3 == 0:
    array = array + a
  if b/3 == 0:
    array = array + b

Still not intended output
a = 4401
b = 8832
c = b - a
array = [] # Corrected: Initialized as an empty list
for i in range (c):
  if a % 2 == 1: # Check if 'a' is divisible by 3
    array.append(a)
  a += 1 # Increment 'a' for the next iteration, regardless of if condition

number = sum(array)
print (number)
print (array)
after some correction this should give the right input.
