
#Python Dictionaries

The last data structure you will learn about in Python is similar to the last data structure you learned about in JavaScript.

In JavaScript,objects are able to hold multiple key:value pairs, which make them extremely robust. A value could hold any data type, including methods.
```
var dog = {
        toys: ["Bone", "Ball", "Rope"],
        age: 5,
        species: "Golden Doodle",
        bark : function() {
         return "Woof";
         }
        }
```

In Python (along with many other languages), these types of data structures are called dictionaries.


## Objectives:
+ Understand Python Dictionary Syntax
+ Compare Dictionaries vs Lists


## Dictionaries
When you open up a dictionary, what do you see? Words and their definitions. Dictionaries work like that - they contain pairs of keys, which are usually words, and values (their definitions). Dictionaries are like lists, but instead of having numbers as indexes, the indexes are something else - usually strings. Check it out:

<img src="https://raw.githubusercontent.com/learn-co-curriculum/cssi-4.10-python-dictionaries/master/images/dictionary.png">

In this example, we can associate each of the items on our grocery list with its price. We don't really care about the order of the grocery list - it is way more helpful to know how much each item will cost!

A key in a dictionary must be unique and associated with a value.

How do we use them? The Python syntax for declaring a dictionary is with {curly brackets}. To create an empty dictionary, just set a variable equal to curly braces:
```
empty_dict = {}
```
To create a dictionary with values in it, set key-value pairs separated by colons and commas:
```
my_cart = {'Eggs': 2.59,
'Milk': 3.19,
'Cheese': 4.80,
'Yogurt': 1.35,
'Butter': 2.59,
'More Cheese':6.19 }
```

## Key-Value Pairs
Key-value pairs are separated by commas. Keys are generally strings, and their associated values can be of any data type.
```
cartoon_species = {'bugs': 'rabbit',
           	       'elmer': 'human',
                   'wiley e': 'coyote',
       	           'tom': 'cat',
      	           'jerry': 'mouse'}
```
***Keys*** are on the left of the colons (‘bugs’, ‘elmer’, ‘wiley’, ‘tomas’, ‘jerry’)
***Values*** are on the right of the colons (‘rabbit’,‘human’,‘coyote’,‘cat’, ‘mouse’)

Just as in a regular dictionary, the keys must be unique, otherwise the program will throw an error.
```
cartoon_species = {'bugs': 'rabbit',
      	   'bugs': 'bunny'}

cartoon_species
>> {'bugs': 'bunny'}
```
Also, it doesn't make sense to have two different values for the same key, so Python will only use the last key-value pair if two or more are used. **Important: Do not re-use keys in your dictionaries!**

## Accessing Values in a Dictionary
In order to access the values of a dictionary, you want to pass the key to the dictionary and it will return the value.
```
cartoon_species = {'bugs': 'rabbit',
           	       'elmer': 'human',
                   'wiley e': 'coyote',
       	           'tom': 'cat',
      	           'jerry': 'mouse'}

print cartoon_species['elmer']
>> "human"
```
## Updating a Dictionary
To modify the values inside a dictionary use the assignment operator and send it the key value.
```
cartoon_species = {'bugs': 'rabbit',
           	       'elmer': 'human',
                   'wiley e': 'coyote',
       	           'tom': 'cat',
      	           'jerry': 'mouse'}

cartoon_species['bugs'] = 'bunny' #reassigns "rabbit" to "bunny"
```

You can also use this technique to add key-value pairs to a dictionary that don’t already exist. For instance, with my_dict, I could do the following:
```
cartoon_species['tweety'] = ‘bird’
print cartoon_species

{'tom': 'cat', 'wiley e': 'coyote', 'elmer': 'human', 'bugs': 'bunny', 'jerry': 'mouse', 'tweety': 'bird'}
```
The {"tweety": "bird"} key-value pair has now been added to cartoon_species.

#Common Dictionary Operations
```
len(cartoon_species)
5 # Shows the number of key-value pairs in a dictionary.

cartoon_species.clear()
{} # Clears the dictionary

del cartoon_species['bugs'] #Delete a key-value pair from the dictionary
{‘elmer’: ‘human’,
‘wiley e’: ‘coyote’,
‘tom’: ‘cat’,
‘jerry’: ‘mouse’}



```
## Searching for a Key in a Dictionary
What if you wanted to check if the key 'jerry' was in cartoon_species?  Use the in operator.
```
if 'jerry' in cartoon_species:
 print 'Hi Jerry!'
```
This only works for keys in a dictionary, not the values.

## Looping over a dictionary
It is often useful to be able to loop over the contents of a dictionary. Using the for-in loop we would write:
```
for cartoon in cartoon_species:
 print cartoon
```
What do you notice? What is it printing? It’s printing the keys!
```
bugs
elmer
wiley e
tom
jerry
```
How would you print the values? Combine the technique of accessing the dictionary through the key:
```
for cartoon in cartoon_species:
 print cartoon_species[cartoon]
```
This prints:
```
rabbit
human
coyote
cat
mouse
```

## Conclusion
Remember dictionaries are just like lists but rather than having and index (0,1,2,3) you have keys for each value. Dictionaries become extremely important when wanting to create and store large amounts of data of varying types.
