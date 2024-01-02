In the previous section, we saw the difference between **primitive data structure** (string, integer, floating-point number, and boolean) and **collection data structure** (list, dictionary, set, tuple). 

The **primitive data structure** can be think of as the *building blocks* of collection data structures while **collection data structure** allows *multiple pieces of primitive data to be stored* together within the same structure. You need primitive data structure to build a collection data structure. **Here's a quick summary comparing between the two**:

|| Primitive | Collection |
|--|--|--|
|Types|`int`, `str`, `float`, `bool`  |`list`, `tuple`, `dict`, `set`  |
|Examples|`"cat"`, `0.04`, `False`  |`myList = [1, 2, 3]`, `mySet = {44, 3, 0}`  |
|Amount of Data Stored|Single value, can't be blank |Mutiple values, blanks allowed  |
|Type of Data Stored|Single type, specific   |Multiple types, Mix types allowed  |
|Memory use|One memory slot under one variable  |Multiple memory slots under one variable, slots do not need to be contiguous  |


When designing a program, it is very important to think ahead about
 1. **what kind** the data does the program need to process 
 2. **how many** pieces of data does the program need to process 
 3. **how will the data be processed** by the program.

If the program is a simple guess the number game that doesn't store high scores or player names, **primitive data structure** is more than enough to handle the demand of the program. However, if the program **stores, process, updates, and manipulate data** as part of its core functionality, a **collection data structure** is most likely needed. The question becomes: _which collection data structure do you use?_

---
## List: *Ordered, Mutable, Duplicates allowed, index-referenced*
A **list** is a type of collection data structure that stores data in an **ordered** (sequenced) manner and allows for those data to be changed (**mutable**)

To create a list in Python, use a square bracket `[]` around the elements you want to store. Each element in the list should be *separated by comma*.

    animals = ["lion", "tiger", "elephant", "flamingo", "hippo", "lemur"]
Each element in the list can be referenced using the **index** of the value. The index indicates where in the sequence was the data stored. In Python, **the first element stored in the list is assigned with the index of 0**. Any subsequent elements are assigned the next positive integer index in the list (1, 2, 3, 4, etc.)

> **On AP CSP Exam, the first element in a list has an index of 1.** 

The list `animals` contains 6 elements. **In Python**, the first element, `"lion"`, is assigned the index of 0 with the last element, `"lemur"`, assigned the index of 5 (not 6!). However, **on the AP Exam**, `"lion"` would have an index of 1 and `"lemur"` would have an index of 6.

| **elements** 	| lion 	| tiger 	| elephant 	| flamingo 	| hippo 	| lemur 	|
|:------------:	|:----:	|:-----:	|:--------:	|:--------:	|:-----:	|:-----:	|
|   **Index**  	|   0  	|   1   	|     2    	|     3    	|   4   	|   5   	|


The list is **mutable**. This means once the list is created, you can still *add, remove, rearrange, and change the values* of the element as you wish. Also, **list elements do not need to be unique**, you can have duplicated values inside a list and the program will treat them as different elements.
```python3.run
animals = ["lion", "tiger", "elephant", "flamingo", "hippo", "lemur"]

animals.append("giraffe")
animals.append("elephant")

print (animals)

for i in range(len(animals)):
    animals[i]+="s"

print (animals)
```
In the code segments above, I **added (append)** "giraffe" and "elephant" to the list after creating it. Notice how the list still accepts "elephant" even though it is a duplicated value. I am also allowed to iterate through the list with a for-loop to concatenate "s" to the end of each string values in the list.


The indexed nature of list makes it possible to reference elements inside the list using its index. This allows us to locate a specific element in the list to either *edit the element, remove the element, or rearrange the element* as needed. The ordered nature of the list means each element has an assigned position in the list and that position does not change unless we change it. 

Finally, list elements can be **any primitive data types** and **collection data type.** `favoriteNumbers = [10, 20, 30, 40]` and `togetherThings = [["bread", "butter"], ["pencil", "eraser"], ["burger", "fries"]]` are both acceptable way to create lists. 

You can also mix and match different data types like the following examples:

    scottPilgrim = ["Scott", "Pilgrim", 24, ["Power of Understanding", "Power of Love", "Power of Self-Respect"], 2.10, True]
    matthewPatel = ["Matthew", "Patel", 24, ["Mytical", "Levitation", "Pyrokinesis", "Demon Hipster Chicks"], 2.10, False]

Because data is ordered in a list, if I store similar data in the same position across different lists, I can do something fun like this:

    # Character Stats for first evil ex battle
    	scottPilgrim = ["Scott", "Pilgrim", 24, ["Power of Understanding", "Power of Love", "Power of Self-Respect"], 2.10, True]
    	matthewPatel = ["Matthew", "Patel", 24, ["Mytical", "Levitation", "Pyrokinesis", "Demon Hipster Chicks"], 2.10, False]
    
    # Store characters in a list together
    	firstBattle = [scottPilgrim, matthewPatel]
    
    # Iterater through the list and display stats
    	for character in firstBattle:
    	    print ("First Name: ", character[0])
    	    print ("Last Name: ", character[1])
    	    print ("Age: ", character[2])
    	    print ("Powers: ", character[3])
    	    print ("Loot value:$", character[4])
    	    print ("Winner?: ", character[5])
    	    print ()

## Considerations for choosing list as your data structure
While a list is versatile and simple to use, it is more suitable for certain data structure and program functionalities. Before implementing any data structure for your CPT, you should have planned out the purpose and functionality of your program along with the data it will process.
### A list ==might== be for you if the following applies:

 - [ ] **Ordered Data**: Use a list if the order of your data is important and you need to maintain this sequence.
 - [ ] **Mutable Data**: Choose a list if you need to modify the data (add, remove, change elements) after it's created.
 - [ ] **Duplicates Allowed**: If your data can have duplicates (same value appearing more than once), a list is suitable.
 - [ ] **Variable Length**: Use a list if the number of elements in your collection might change over time.
 - [ ] **Heterogeneous Data**: If your collection will contain different types of data (e.g., integers, strings, other lists), a list is a good choice.
 - [ ] **Index-Based Operations**: Choose a list if you need to perform operations based on element indices (e.g., retrieving the third item).
### A list ==might not== be suitable if the following applies:
 - [ ] **Non-Ordered Data**: Avoid lists if the order of data is not important and a set or dictionary could be more efficient.
 - [ ] **Immutable Data**: If your collection of data should not change after it’s created, consider using a tuple instead.
 - [ ]  **Unique Elements Only**: If each element must be unique (no duplicates allowed), a set might be a better option.
 - [ ]  **Key-Value Pairs**: Don’t use a list if you need to associate each piece of data with a unique key; a dictionary is more suitable in this case.
 - [ ] **Memory Efficiency**: For very large collections of data where memory usage is a concern, explore other data structures that might be more memory-efficient.
