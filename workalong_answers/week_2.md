# Python for Librarians Workalong answers - Week 2

## Question 1

Describe what the `int()` function does in the following markdown cell 

*Answer:* Turn the value you pass to it into an integer. Useful when changing strings into integers for when we compare them to other integers.


## Question 2

Describe what the `input()` function does in the following markdown cell.

*Answer:* Prompt the user to to input a value via the keyboard. This values is kept as a string.

## Question 3

Fix the following cell so that it prints _They are the same!_.

(Hint: there are at least two ways to do this)


```python
number = "4"

if int(number) == 4:
    print("They are the same!")
```


## Question 4

Complete the following function that will find the maximum value in a list of integers.


(Hint: you only need to modify lines: 11 & 17)

```python

numbers = [2, 5, 2, 9]

def findMax(numbers_to_consider):

    # We will start with automatically setting the highest number
    # to the first value in our list.
    # (or in other words: the number at the 0 index in the list)
    max_number = numbers_to_consider[0]

    for n in numbers_to_consider:
        if  n > max_number:
            max_number = n

    return max_number


result = findMax(numbers)
print("Largest number is: ")
print(result)


```


## Question 5

Complete the following function that will find the smallest value in a list of integers. (Hint: you only need to modify lines: 11 & 15)

```python

numbers = [2, 5, 2, 9]

def findMin(numbers_to_consider):


    # We will start with automatically setting the highest number
    # to the first value in our list.
    # (or in other words: the number at the 0 index in the list)
    min_number = numbers_to_consider[0]

    for n in numbers:
        if n < min_number:
            min_number = n

    return min_number


result = findMin(numbers)
print("Smallest number is: ")
print(result)

```

## Question 6

Complete the following cell to find out the average (or mean) of the **Total Checkouts** column?

```python

sfl_data["Total Checkouts"].mean()

```

## Question 7

Complete the following cell to find out the highest number of **Total Checkout** for a patron.

```python

sfl_data["Total Checkouts"].max()

```


## Question 8

In the cell below reflect on the two code cells above about average checkouts between 2015 & 2016. What can you say about them?

*Answer:* People who created accounts in 2015 checked out and renewed more material on average compared to people who created an account in 2016. What did the Library do diﬀerent in 2015 I wonder?

## Question 9

In the markdown cell below describe your observations about Adult versus Juvenile borrowers for the Main Library based on all of the different examples we saw above.

*Answer:* You could probably say it in many ways but one solution is, Juvenile's on average check out more material and peform more renewals over adults.

## Question 10

If we want to see if either of two conditional is true (eg. `OR`) we combine them with `|`. Complete the following code cell so it counts how many patrons are in the main library `or` Chinatown

```python

sfl_data[(sfl_data["Home Library Definition"] == "Main Library") \
         (sfl_data["Home Library Definition"] == "Chinatown")].count(numeric_only=True)

```

## Question 11

Can you find what the average number of checkouts for adult borrowers at the Glen Park library?

```python

sfl_data[(sfl_data["Home Library Definition"] == "Glen Park") & \
        (sfl_data["Patron Type Definition"] == "ADULT")].mean()

```

## Question 12

Can you find the the highest number of checkouts for adult borrowers at the Main Library or Chinatown?

```python

fl_data[((sfl_data["Home Library Definition"] == "Main Library") | \
        (sfl_data["Home Library Definition"] == "Chinatown")) &
        (sfl_data["Patron Type Definition"] == "ADULT")]["Total Checkouts"].max()

```

## Question 13

Take a moment to look at the data you've look at so far. See if you can come up with another interesting calculation put it in the cell below, and add to the comment to describe what you've found.


*Answer:* I do not have a particular answer in mind here, I'm just hoping you will explore the data with some interesting selection statements.

### Question 14

After reading up on what a correlation matrix is, what can you say about the data in the SF Library user data? Add some thoughts in the markdown cell below. (You'll note that much like as when we use `describe()` calculating the correlation matrix is done automatically on just numeric data in the dataset.

*Answer:* The correlation matrix tell me that

Many things, but for a start:

- Total Renewals is postively correlated with Total Checkouts
- Year Patron Registered is negatively correlated with Year Patron Registered
- Year Patron Registered is negatively correlated with Total Renewals