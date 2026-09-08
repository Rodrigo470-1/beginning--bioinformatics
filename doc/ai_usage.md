# AI Use Log
- Tool/model & version:
- What I asked for:
- Snippet of prompt(s):
- What I changed before committing:
- How I verified correctness (tests, sample data)

Model: Gemini 2.5 Flash

I originally proposed this code to solve problem 2 : 

array = ['HumptyDumptysatonawallHumptyDumptyhadagreatfallAlltheKingshorsesandalltheKingsmenCouldntputHumptyDumptyinhisplaceagain.']
c = array [22:28] + array [97:103]
print (c)

Which then later I asked gemini to help me understand what was wrong and added this lines of code lines : 

string_to_slice = array[0]
c = string_to_slice[22:28] + ' ' + string_to_slice[97:103]
explaining that it was trying to slice the list, but not the string itself.
After I just tried with the example rosalind have to see if it worked.

3rd 
Original
a = input
b = input
  if a/3 == 0:
    array = array + a
  if b/3 == 0:
    array = array + b
  
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

Still not intended output, so I stop and saw that I did not needed to increase b as well and added to the list.
a = 4401
b = 8832
c = b - a
array = [] 
for i in range (c):
  if a % 2 == 1: 
    array.append(a)
  a += 1 #

number = sum(array)
print (number)
print (array)
after some correction this should give the right output, I tried again with another sample data from Rosalind and the ouput was close, but not the desired value, I need to re-evaluate.


#5
Original code:
input = "We tried list and we tried dicts also we tried Zen"
d ={}
c = 0
for output in input.split():
 d [output] = ''
 print (d) # I tried to use this to debug and see what the for loop was doing.
 if output in d:
  d[output] = c+1
 #if output != input.split():

print (d)
after some struggling and asking Gemini 2.5 what was I missing it gave me .get part of the code which I didn't knew and pointed out some logical issues on the original code, like overwriting some variables and how I was replacing with 0 any non-matching part, and I was just getting the word and a 1 and it did not move forward until the prompt to Gemini.
This was the last iteration I arrived
input = "We tried list and we tried dicts also we tried Zen"
d ={}
for output in input.split():
 d [output] = d.get(output, 0) + 1
for output, c in d.items():
 print (output, c)

  
print (d)

#6

