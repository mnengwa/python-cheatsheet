# LISTS, TUPLES, DICTIONARIES

#### Data types that allows us to hold a collection of related items

### Built-in functions
> `len(<object>)` gets length - list, tuples, dictionary 
> `type(<object>)` gets data type - list, tuples, dictionary 

# LISTS
> synonymous to **`arrays`** in JavaScript and many other languages.

> They can contain any number of items including zero, and as much as your system memory can hold

> A given list can hold a mixture of data types i.e numbers, strings, functions, other lists, tuples etc

## Comparison
```python
# Lists that contain the same elements in the same order are equal
print(['a', 'e', 'i', 'o', 'u'] == ['a', 'e', 'i', 'o', 'u'])

# Otherwise they are seen as different values by the interpreter
print(['a', 'e', 'i', 'o', 'u'] == ['e', 'a', 'i', 'o', 'u'])
```

## Indexing
```python
# Array indices start from zero like the array of JavaScript
# A negative index can also be used to access elements

# E.g we have an array of the 5 vowels
vowels = ['a', 'e', 'i', 'o', 'u']

# Get the first item
vowels[0]
vowels[-5]

# Get the last item
vowels[4]
vowels[-1]

# Get the first two
vowels[0:2]

# Get the third to the fourth
vowels[1:4]

# Get the last two
vowels[3:5]
```

## Nesting
```python
# Lists can contain other lists

# E.g Looping through a list
cohorts = ['cohort 54', 'cohort 55', 'cohort 56', 'cohort 57', 'cohort 58']
for index, cohort in enumerate(cohorts):
    print(f'{index+1}. {cohort}')

communities = [
    ['KENYA', 'TANZANIA', 'UGANDA', 'RWANDA', 'BURUNDI', 'REPUBLIC OF SOUTH SUDAN', 'DEMOCRATIC REPUBLIC OF THE CONGO'], 
    ['ANGOLA', 'BOTSWANA', 'COMOROS', 'ESWATINI', 'LESOTHO', 'MADAGASCAR', 'MALAWI', 'MAURITIUS', 'MOZAMBIQUE', 'NAMIBIA', 'SEYCHELLES', 'SOUTH AFRICA', 'ZAMBIA', 'ZIMBABWE'],
    ['BENIN', 'BURKINA FASO', 'CABO VERDE', 'CÔTE D\'IVOIRE', 'THE GAMBIA', 'GHANA', 'GUINEA', 'GUINEA BISSAU', 'LIBERIA', 'MALI', 'NIGER', 'NIGERIA', 'SENEGAL', 'SIERRA LEONE', 'TOGO']
]
for communityIndex, community in enumerate(communities):
    print(f'{communityIndex+1}. {community}')
    for countryIndex, country in enumerate(community):
        print(f'{countryIndex}. {country}')
```

## Manipulation
```python
avengers = ['Peter Parker', 'Thor', 'Ant Man', 'Hawk Eye', 'Black Widow', 'Wanda', 'Ultron', 'Vision']

# Replace the 'Peter Parker' with 'Spider Man'
avengers[0] = 'Spider Man'

# The number of items inserted DO NOT NEED TO BE EQUAL to the number replaced
# E.g Replace the last 2 with 3 more
avengers[6:8] = ['Doctor Strange', 'Guardian Of The Galaxy', 'Captain Marvel']

# E.g Replace the last 3 with 1 item
avengers[7:10] = ['Nick Fury']

# Remove 'Ant Man''
del avengers[2]

# Add one item at the end
avengers.append('Peter Quil')

# Add many items at the end
avengers.extend(['Rocket', 'Gamora', 'Drax The Destroyer'])

# Insert an item at a specific index
# The remaining list items are pushed to the right
avengers.insert(2, 'Loki')

# Remove an item at a specific index
# An exception is raised if the item does not exist
avengers.remove('Loki')

# Remove the last item
# Returns the item removed
last = avengers.pop()

# You can give it an index
first = avengers.pop(1)

# Join multiple lists together
fantastic_four = ['Mister Fantastic', 'Invisible Woman', 'The Human Torch', 'The Thing']
heroes = avengers + fantastic_four
```

# TUPLES
> A data type that allows us to hold a collection of related items. Unlike lists, tuples are immutable

```python
# creating (packing) a tuple
colours = ('#000000', '#ffffff', '#ff0000', '#00ff00', '#0000ff')
print(f'tuple - {colours}')
print(f'first element - {colours[0]}')
print(f'last element - {colours[-1]}')

# unpacking (destructuring) a tuple
# the number of variables on the left MUST match the number of values in the tuple
# otherwise an exception is raised
(black, white, red, green, blue) = colours

# packing & unpacking can be combined into a single statement
(black, white, red, green, blue) = ('#000000', '#ffffff', '#ff0000', '#00ff00', '#0000ff')
```

## Looping
```python
colours = ('#000000', '#ffffff', '#ff0000', '#00ff00', '#0000ff')

for index, colour in enumerate(colours):
    print(f'{index+1}. {colour}')
```

# DICTIONARY
> Dictionaries are used to store data values in **key**:**value** pairs
> Unlike lists & tuples DUPLICATES ARE NOT ALLOWED

## Defining, accessing, updating dictionaries
```python
# Defining
him = {
    "age": 22,
    "sex": "male",
    "name": "Unknown",
}

her = person = {
    "age": 22,
    "sex": "female",
    "name": "Unknown",
}

# Access values
his_name = him["name"]
her_name = her["name"]

# Change values
him["name"] = "John Doe"
her["name"] = "Jane Doe"

# Add new keys
him["nationality"] = "Kenyan" 
her["nationality"] = "Tanzanian" 

# Update values
him.update({"age": 25, "sex": "MALE"})
her.update({"age": 26, "sex": "FEMALE"})

# Remove keys
him.pop("age")
her.pop("age")
```

## Looping through dictionaries
```python
country = {
    "name": "Kenya",
    "capital": "Nairobi",
    "size": "580,367 kilometer squared"
}

# Loop through all keys
for key in country:
  print(key)

for key in country.keys():
  print(key)

# Loop through all values
for key in country:
  print(country[key])
  
for value in country.values():
  print(value)

# Loop through all key & values
for key in country:
  print(f'{key} - {country[key]}')
  
for key, value in country.items():
  print(f'{key} - {value}')
```

## Creating copies
```python
kenya = {
    "name": "Kenya",
    "capital": "Nairobi",
    "continent": "Africa",
    "size": "580,367 kilometer squared"
}

print(kenya)

# tanzania = kenya WON'T create a new dictionary but reference it "as a new variable name"
# so to create a copy that you can manipulate separately...
tanzania = kenya.copy()
tanzania["name"] = "Tanzania"
tanzania["capital"] = "Dodoma"
tanzania["size"] = "945,087 kilometer squared"

print(tanzania)
```

> Read more about dictionary methods
> `popitem()` - removes the last inserted key-value pair
> `clear()`	- removes all the elements from the dictionary
> `fromkeys()` - returns a dictionary with the specified keys and value
> `setdefault()` - returns the value of the specified key. If the key does not exist: insert the key, with the specified value