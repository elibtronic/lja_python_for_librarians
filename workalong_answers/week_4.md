# Python for Librarians Workalong answers - Week 4

## Question 1

We see in our top 10 cities an entry for `Ville de Québec` let's change that the english version of that name `Quebec City`

Modify the following code cell to do this.

```python

CSH_data.loc[CSH_data['city'] == "Ville de Québec", 'city'] = "Quebec City"

```


## Question 2

Does that first entry look familiar?

*Answer:* Our old pal Elsvier again!

## Question 3

Complete the code to show the frequency of different days in the dataset.

```python

CSH_data['day_of_week'].value_counts()

```

## Question 3 (continued)

The day of the week with the most downloads is... (fill in with your answer)

*Answer:* Looks like Tuesday is when most of the downloads happen, but the margin is small.


## Question 4

Complete the code to show the frequency of downloads associated with top publishers.

```python

CSH_data["top_pub"].value_counts()

```


## Question 4 (continued)

What percentage of downloads are associated with the top 10 publishers. (There is multiple ways to answer this so complete it however feels best for you.

```python

percent_top = len(CSH_data[CSH_data["top_pub"] == True]) / len(CSH_data)
print(percent_top)

```


## Question 5

In what month is the highest rate of downloads occur?

*Answer:* Looks like the 8th week of the year, which is some point in February.


## Question 6

Fill in the code cell below to draw out a pie graph of the top 10 publishers found in this data.

```python

prop_publisher = CSH_data["top_pub"].value_counts().head()
prop_publisher
fig = px.pie(prop_publisher, \
             values = prop_publisher.values, \
             names = prop_publisher.index, \
             title = "Portion of top 10 publishers in the data")
fig.show()

```

### Question 7

Can you summarize some details about the differences in the two pie graphs we have looked at here?

*Answer:* It looks like the popular articles are downloaded mostly on Wednesday and Tuesday and almost never on a Thursday or Friday wherein in the whole collection of articles they are downloaded almost evenly by each day.