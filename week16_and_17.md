# Week 16 and 17

## Algorithms Workshop - Data Structure Design
* From last time: data get stored where ever there is space
* array stored in sequential space in memory

Example
* Finding whether there is an item with a value of 17 in the array you have to check every item so the complexity is linear time. 

* An alternative data structure (rather than an array) would be to store the 17 in an address position of memory with a value of 17. Then the look up will be in constant time. Although there are issues:
-- This would take up a lot of memory space
-- what do you do with new numbers out of scope?
-- non-unique numbers
-- collisions

* say you only have a block of memory of 21
* how do you store number 21? You can use % length of the size of the array (21) and so it gets stored at index 0.

* this is called a hash table (in C# and Java, in ruby, python and javascript it is a set).

* Another way to handle collisions is that in the place memory you refer to an address of another block of memory where another array is with all the colliding items. 
* A Hash table stored in memory is 3 times the size of the equivalent array, but that is not too big of a problem. 
* You cannot solve the problem of non-unique numbers with a hash table


* The above is with integers. If you were using strings you could have a formula that works out the index of the hash (for example, it could be the sum of the value of the letters' character references).

### Hashing

* When you hash a password you cannot unhash it
* However, when you encrypt a password it can be decrypted

- e.g.s
```1,1,1 => '3times1'```
you can decrypt
```1,1,1 => 'startswith1'```
you have lost information, but still have some information. Because information is lost it cannot be decrypted


