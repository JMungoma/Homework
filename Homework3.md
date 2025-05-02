## 1. What is an algorithm?
An algorithm is a series of logical steps followed to solve a problem. 

## 2. Variable names may not start with certain characters - name two.
A variable cannot start with (1) a number and (2) reserved names/keywords

## 3. What is a Semantic error?
A semantic error is when the code is grammatically correct but it does not make sense to produce the expected results.


## 4. What is the #1 rule of coding / debugging?
Complexity is the enemy of efficiency, keep it simple.

## 5. List 5 Python reserved words.
The 5 python reserved words are: False, None, Try, Import, Class

## 6. Write a multi-line string with your name, favorite food, and dream job on 3 different lines

FName, LName = "Joseph", "Mungoma"

FavFood = "Matoke"

DreamJob = "IT Specialist"

print("First Name:",FName, ", " "Last Name:",LName ) 
print("Favorite Food:", FavFood)
print("Dream Job: " , DreamJob)

## Output
First Name: Joseph , Last Name: Mungoma
Favorite Food: Matoke
Dream Job:  IT Specialist

## 7. Assign 5 different data types to 5 different variables. At least one datatype must be a string  

z = str("It's a beautiful day in the neighbourhood")
x = int(43.8)
c = float (50)
o = ["Keyboard", "Mouse", "Monitor", "System Unit"]
i = True

## Print the length of your string
print("The length of z is ", len(z))

## Print the index value of the 4th character in your string
print("The 4th index value in z string = ", z[3])

# Output
The length of z is  41
The 4th index value in z string =  s

## 8. Create a new variable called savvy, and assign it the string with this phrase "Learning Data Analytics and Python is Awesome!"

savvy = "Learning Data Analytics and Python is Awesome!"

## Return a range of characters that slices the above string from the beginning of  "ing" up to before "and"

print(savvy[5:-22])

## Replace "Awesome" with "great" in the string
## Test and print the savvy string to see it contains "Python"
print(savvy.replace("Awesome", "Great"))

    
## 9. Create and assign 3 more variables called name, age and length using the multi-variable naming method
name = "Dexter"
age = float(18)
length = 45

## Format a new string called 'miniBio' using variables in curly brackets to complete this phrase... "Hi my name is (name), I am (tall) and (so) old today."
## Print 'miniBio'

miniBio = "Hi my name is {}, I am {} inches tall and {} years old today. "
print(miniBio.format(name, length, age))

## Cast and print the age variable to a float

name = "Dexter"
age = float(18)
length = 45

miniBio = "Hi my name is {}, I am {} inches tall and {} years old today. "
print(miniBio.format(name, length, age))


## 10. Create a list of at least 5 elements of mixed data types.

anatomy = ["body", 2.0, {"Number of fingers": "5 total"}, True, "parts"]
print(("Composition of the anatomy is: "), anatomy)

## Replace a part of it with something else

anatomy = ["body", 2.0, {"Number of fingers": "5 total"}, True, "parts"]
anatomy[3] = "False"
print("Boolean replace with: ", anatomy)

## Append or insert several more items to the list



## Find and print the length of the list

anatomy = ["body", 2.0, {"Number of fingers": "5 total"}, True, "parts"]
print("Length of anatomy list = ",len(anatomy))


## Slice a sub-section of the 1st list, and save it to a different 2nd list
## Print the 2nd list
arms = anatomy[2:-1]
print(arms)

## Extend your original list with the 2nd list sliced above

anatomy.extend(arms)
print(anatomy)

## Create a new list called "simList" containing at least 5 elements of the same data type, either string, integer, float, or Boolean
## Sort "simList", and print the list

simList = [40, 20, 160, 200, 10]
simList.sort()
print(simList)

## Copy the "simList" list to another 3rd list
athirdList = simList.copy()

## Add the 2nd and 3rd lists together into a 4th list
fourthList = athirdList + simList
print(fourthList)



## 11. Create a tuple of about 5 elements
## Multiply your tuple by 3 and save it to a new 2nd tuple

tools = ('saw', 'hammer' , '12-gauge wire', 'wood', 'screwdriver') 
xtools = tools * 3

## Access and print the 12th element from the 2nd tuple

tools = ('saw', 'hammer' , 12, 'wood', 'screwdriver') 
xtools = tools * 3
print('The 12th element of this tuple is...', xtools[12])

## Sort the 2nd tuple and print it

tools = (1, 8 , 12, 9, 6) 
xtools = tools * 3
sorted(xtools)
print('Sorted tuple list is...', xtools)


Copy 4 specific elements from your 2nd tuple to a new 3nd tuple




Unpack the 3rd tuple into 4 variables and print these variables

Create a 4th tuple with single item 50 and print this tuple

Add the 2nd and 3rd tuple together into a 5th tuple and print the tuple

tools = 'saw', 
tools = ('saw', 'hammer' , '12-gauge wire', 'wood', 'screwdriver') 
xtools = tools * 3

print(xtools)


13. Create a dictionary with at least 5 values of different data types
playlist = {
    "artist": "New Era",
    "album": "Omega",
    "genre": "Blues",
    "year": 1986
}
print("Joe's playlist is: ", playlist)

## Print out 1 value
playlist = {
    "artist": "New Era",
    "album": "Omega",
    "genre": "Blues",
    "year": 1986
}
playlist["album"]

## Replace any one value in your dictionary with your name
playlist = {
    "artist": "New Era",
    "album": "Omega",
    "genre": "Blues",
    "year": 1986
}
playlist["artist"] = "Joe"
playlist["artist"]

## Add your favorite color to the dictionary

playlist.update(color="gold")
playlist["color"]

## Add a list, tuple or set to your dictionary

playlist = {
    "artist": "New Era",
    "album": "Omega",
    "genre": "Blues",
    "year": 1986,
    ("J.Green", "A.Smith", "I.Carpenter"): "composers"
}
print(playlist)

## Print a list of the dictionary keys

playlist = {
    "artist": "New Era",
    "album": "Omega",
    "genre": "Blues",
    "year": 1986,
    ("J.Green", "A.Smith", "I.Carpenter"): "composers"
}
keys = playlist.keys()
list(keys)

## Print a list of the dictionary values

playlist = {
    "artist": "New Era",
    "album": "Omega",
    "genre": "Blues",
    "year": 1986,
    ("J.Green", "A.Smith", "I.Carpenter"): "composers"
}
values = playlist.values()
list(values)

## Copy your 1st dictionary into a 2nd dictionary

playlist = {
    "artist": "New Era",
    "album": "Omega",
    "genre": "Blues",
    "year": 1986,
    ("J.Green", "A.Smith", "I.Carpenter"): "composers"
}
musicdict = playlist.copy()

## Pop an item from the 2nd dictionary, and print the dictionary
playlist = {
    "artist": "New Era",
    "album": "Omega",
    "genre": "Blues",
    "year": 1986,
    ("J.Green", "A.Smith", "I.Carpenter"): "composers"
}
musicdict = playlist.copy()
item = musicdict.popitem()
print(item)
print(musicdict)

## Remove all the elements from the 2nd dictionary and print the result

musicdict = playlist.copy()
musicdict.clear()
print("Music dictionary after clear: ", musicdict)