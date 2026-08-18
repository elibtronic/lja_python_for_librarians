# Python for Librarians Workalong answers - Week 1


## Question 1

Complete the code cell below to set the variable age equal to your age in years.

```python
#Tim's age in 2026...
age = 46
```

## Question 2
Add your new variable age to the print function below to print it to the screen. To do this please add the variable age to the print statement below by typing it in between the brackets.

```python
print(age)
```

## Question 3
Can you print Mom's phone number to the screen, by adding the key into the code cell below?

```python
print(phone_numbers["Mom"])
```

### Question 4
Can print Joe's phone number to the screen using the cell below?

```python
print(phone_numbers["Joe"])
```

### Question 5
Can you print out Thursday's temp in F?

```python
print(toronto_weather["Thursday"] * 9/5 + 32)
```

### Question 6
Can you complete the following expression to find out the average temp from the weekend?

```python
weekend_average = (toronto_weather["Saturday"] + toronto_weather["Sunday"] ) / 2
print(weekend_average)
```

### Question 7
Can you print how many days you have been alive for (approximately) using the age variable in the following cell?

```python
age = 41 * 365
print(age)
```

### Question 8
If you had 45 donuts and you were putting them into boxes that could hold 12 donuts, how many donuts would be in the last box?

```python
lastbox = 45 % 12
print(lastbox)
```

### Question 9
Python uses brackets just like in algebra class. Add some round brackets, which look like: ( and ) to the following statements so that it actually prints out the average of the numbers: 10, 15, 20, 10, 15

```python
average = (10 + 15 + 20 + 10 + 15) / 5
print(average)
```

### Question 11
Can you finish the following loop to print all of the numbers in the list variable called `numbers` in the following cell?

```python
numbers = [1,2,3,4,5]
for digit in numbers:
    print(digit)
```

### Question 12
Python is pretty smart and will loop through anything that looks like it can be looped through. With a list it will loop through all of the items in the list. With a string variable it will loop through all of the letters found in the string.

Can you complete the loop in the next cell so that it prints the letters of Captain Kirk's name?

```python

name = "James Tiberius Kirk"

for letter in names:
    print(letter)


```

### Question 13
Let's try one a little more challenging. Can you write a loop in the following cell that will print each letter of the string variable called alphabet ? You need to completed lines 3 & 4.

```python
alphabet = "abcdefghijklmnopqrstuvwxyz"

for letter in alphabet:
    print(letter)
```

### Question 14

Let's try to print out each key and the corresponding value for that key so the results look something like the following:

`QC -> Quebec`

We'll use a loop to go through each of the keys in our dictionary and then look up each corresponding value. In other words we'll find the full form of the province name by looking up the abbreviation.

You just need to modify line 9.


```python
#we setup our loop to go through the province_look_up dictionary
for abbreviation in province_look_up:
    
    #we lookup the value in the dictionary associated with abbreviation
    #and put it in a variable called full_name
    full_name = province_look_up[abbreviation]
    
    #you need to construct a complex print statement like described above
    print(abbreviation, " -> ",full_name)   

```

### Question 15

Consider the following:

```python

guess = 8

if guess <= 10 and guess >= 1:
    print("Your guess is between 1 - 10")
else:
    print("Your guess is not between 1-10")


```

modify the code in the following cell so that it does the same thing as our example but that it uses `or` instead of `and`. You can assume that `guess` will always be a integer and nothing else. 

Hint: think about how `<=` is like the opposite of `>`


```python
guess = 8

if guess >10 or guess < 1:
    print("Your guess is not between 1-10")
else:
    print("your guess is between 1 - 10")


```


### Extra credit Question!

Try to complete the following code cell. It is the start of a new version of rock/paper/scissors game that uses booleans in the conditionals to make the code shorter. (This is another great example of a lesson you learn about coding, there is often many many different ways to accomplish the same thing.)


```python
# Complete the following cell
# and change the value of player_1 and player_2 to test out the different parts of the new conditional belo
w
#
#pick from the following options
# rock
# paper
# scissors
player_1 = "rock"
player_2 = "rock"
#Tie
if player_1 == player_2:
    print("Tie!")
    
#Player 1 has rock
elif player_1 == "rock" and player_2 == "paper":
    print("Player 2 Wins!")
elif player_1 == "rock" and player_2 == "scissors":
    print("Player 1 Wins!")
    
#Player 1 has paper
elif player_1 == "paper" and player_2 == "rock":
    print("Player 1 Wins!")
elif player_1 == "paper" and player_2 == "scissors":
    print("Player 2 Wins!")
    
#Player 1 has scissor
elif player_1 == "scissors" and player_2 == "rock":
    print("Player 2 Wins!")
elif player_1 == "scissors" and player_2 == "paper":
    print("Player 1 Wins!")