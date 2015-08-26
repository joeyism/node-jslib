# JS Lib

A module that loads some modules that are useful in javascript, for objects and arrays

## Installation

    > npm install --save jslib

## Usage

* [`xcept`](#xcep)
* [`kontains`](#kontains)
* [`keyway`](#keyway)
* [`isUnique`](#isUnique)
* [`getUnique`](#getUnique)

### [xcept](https://github.com/joeyism/node-xcept)

**Object**

Omit object key-values 

    { "a": "some value", "b": "other value", "c": "more value" }.omit(a).omit(c) // { "b": "other value" } 
    { "a": "some value", "b": "other value", "c": "more value" }.except(a).except(c) // { "b": "other value" } 

**Array**

Omit array elements

    [1, 2, 3, 4, 5].omit(1).omit(2).omit(3) // [4, 5]
    [1, 2, 3, 4, 5].except(1).except(2).except(3) // [4, 5]

### [kontains](https://github.com/joeyism/node-kontains)

**Object**

Checks if an object contains an element
    
    {"elm1": "one", "elm2": "two"}.contains("elm1") // true 
    {"elm1": "one", "elm2": "two"}.contains("elm2") // true 
    {"elm1": "one", "elm2": "two"}.contains("one")  // false
    {"elm1": "one", "elm2": "two"}.contains("ELM2") // false

**Array**

Checks if an array contains an element
    
    [1, 2, 3].contains(1)   // true
    [1, 2, 3].contains(one) // false

### [keyway](https://github.com/joeyism/node-keyway)

Transforms an array into an object

    var arr = ["one", "two"];
    obj = Array.keyway(arr) // obj = { "one": "", "two": ""}
    obj = arr.keyway()      // obj = { "one": "", "two": ""}


### [isUnique](https://github.com/joeyism/node-isUnique)
Returns true if the array only has unique elements. Otherwise, return false

    [1].isUnique() // true
    [1,2].isUnique() // true
    [1,1].isUnique() // false

### [getUnique](https://github.com/joeyism/node-isUnique)
Gets the unique version of the array. If there are two matching elements, the latter is removed

    [1].getUnique() // [1] 
    [1,1].getUnique() // [1] 
    [1,2].getUnique() // [1,2]
    [1,2,1,2].getUnique() // [1,2]
    [1,2,2,2].getUnique() // [1,2]


## Versions
**1.1.0**
* added isUnique and getUnique

**1.0.0**
* First working commit
