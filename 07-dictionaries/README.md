# Dictionaries Section Goals

- [Create, access, modify, insert, remove](#create-access-modify-insert-remove)
- [Loop over dictionary keys](#looping-through-dictionaries)
- [Loop over dictionary values](#looping-through-dictionaries)
- [Loop over dictionary values and keys](#looping-through-dictionaries)
- [Clear all values in a dictionary](#clear-all-values-in-a-dictionary)
- [Clear only certain values](#clear-only-certain-values)
- [Get list of keys with a certain value](#get-a-list-of-keys-with-a-certain-value)

## Create, access, modify, insert, remove
```
>>> d = {}
>>> d
{}
>>> type(d)
<class 'dict'>
>>> d = {"first_name": "John"}
>>> d
{'first_name': 'John'}
>>> d["first_name"]
'John'
>>> d["last_name"] = "Smith"
>>> d
{'first_name': 'John', 'last_name': 'Smith'}
>>> d["first_name"]
'John'
>>> d["last_name"]
'Smith'
>>> d["grade"] = 12
>>> d
{'first_name': 'John', 'last_name': 'Smith', 'grade': 12}
>>> d["fav_food"] = "Pizza"
>>> d
{'first_name': 'John', 'last_name': 'Smith', 'grade': 12, 'fav_food': 'Pizza'}
>>> d["grade"] = 13
>>> d
{'first_name': 'John', 'last_name': 'Smith', 'grade': 13, 'fav_food': 'Pizza'}
>>> d.pop("fav_food")
'Pizza'
>>> d
{'first_name': 'John', 'last_name': 'Smith', 'grade': 13}
```

## Looping through dictionaries
```python
student = {
    "first_name": "Frank",
    "last_name": "Smith",
    "grade": 11
}

for key in student.keys():
    print(key)

print()
for val in student.values():
    print(val)

print()
for key, value in student.items():
    print(key, value)
```

## Clear all values in a dictionary
```python
student = {
    "first_name": "Frank",
    "last_name": "Smith",
    "grade": 11,
    "homeroom": "11G"
}

for key in student.keys():
    student[key] = None

print(student)
```

## Clear only certain values
```python
student = {
    "first_name": "Frank",
    "last_name": "Smith",
    "grade": 11,
    "homeroom": "11G"
}

for key in student.keys():
    if "name" in key:
        student[key] = None

print(student)

```

## get-a-list-of-keys-with-a-certain-value
```python
fruit = {
    "apples": 5,
    "pears": 2,
    "plums": 11,
    "peaches": 7
}

shopping_list = []
for fruit, qty in fruit.items():
    if qty <= 5:
        shopping_list.append(fruit)

print(shopping_list)

```
