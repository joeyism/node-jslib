# JS Lib

A module that loads some modules that are useful in javascript, for objects and arrays

## Installation

    > npm install --save jslib

## Usage

* [`xcept`](#xcep)
* [`kontains`](#kontains)
* [`keyway`](#keyway)

### [xcept](https://github.com/joeyism/node-xcept)

**Object**

    { "a": "some value", "b": "other value", "c": "more value" }.omit(a).omit(c) // { "b": "other value" } 
    { "a": "some value", "b": "other value", "c": "more value" }.except(a).except(c) // { "b": "other value" } 

**Array**

    [1, 2, 3, 4, 5].omit(1).omit(2).omit(3) // [4, 5]
    [1, 2, 3, 4, 5].except(1).except(2).except(3) // [4, 5]

### [kontains](https://github.com/joeyism/node-kontains)

**Object**
    
    {"elm1": "one", "elm2": "two"}.contains("elm1") // true 
    {"elm1": "one", "elm2": "two"}.contains("elm2") // true 
    {"elm1": "one", "elm2": "two"}.contains("one")  // false
    {"elm1": "one", "elm2": "two"}.contains("ELM2") // false

**Array**
    
    [1, 2, 3].contains(1)   // true
    [1, 2, 3].contains(one) // false

### [keyway](https://github.com/joeyism/node-keyway)

    var arr = ["one", "two"];
    obj = Array.keyway(arr) // obj = { "one": "", "two": ""}
    obj = arr.keyway()      // obj = { "one": "", "two": ""}


## Versions
**1.0.0**
* First working commit
