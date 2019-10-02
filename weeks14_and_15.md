### Notes from Bob Martin's ['The Future of Programming'](https://www.youtube.com/watch?v=ecIWPzGEbFc)
* Read [this book](https://www.amazon.co.uk/Annotated-Turing-Through-Historic-Computability/dp/0470229055/ref=sr_1_1?adgrpid=52696323789&gclid=EAIaIQobChMI9ueuyefr5AIVg53VCh1nZQBXEAAYASAAEgILTvD_BwE&hvadid=259061355540&hvdev=c&hvlocphy=1006812&hvnetw=g&hvpos=1t1&hvqmt=e&hvrand=16431434418784619476&hvtargid=kwd-300818798325&hydadcr=24427_1748929&keywords=the+annotated+turing&qid=1569408854&sr=8-1)
* Write a 'Floating point package'
* All code is based upon:
-- Assignment Statements
-- If statements 
-- While loops
* What must change?
-- Software professionalism

* Agile manifesto made in 2001 by programmers

* Agile is about disclipline, craftmanship and professionalism.

* Agile is now dominated by business practice

* It is possible the government will try to regulate developers - as we have great responsibility. 
e.g. a car or plane that runs on software can kill people. 
VW blamed the cheating of emmissions tests on developers. 

## Second Algorithm Workshop

### Memory
#### Stores
* Bits: a 1 or a 0
* Bytes: 8 * 1s and 0s (binary), e.g. 26 will look like this as a byte 00011010
* Biggest number you can store in a byte is 255.
* 1 byte = 8 bits
* utf-8 is 1 byte (or 8 bits)
* utf-32 is 4 bytes (or 32 bits)

* What you might be storing in memory:
-- booleans
-- characters
-- addresses
-- numbers
-- characters

e.g.s
```
a = 3
b = a
a += b
>>  b = 3
```
```
a = []
b = a
a << 6
>> b = [6]
```
in the second example b is pointing to the space in memory where the a variable is. In the first example, b is just being set to the VALUE of a. 


* If you see memory as a grid, each cell in the grid has an address. 

* Takes the same amount of time to access one bit of memory compared to another. Doesn't matter what the size of the address is. Therefore, the time is in constant time. The reader points straight to that cell of memory, it doesn't scan throughall the memory. 

* IMPORTANT - There is no address book storing the memory locations. It is stored within the function using it effectively. 
- 'malloc' is what tells your program where there is free memory.

* An array is stored using varying size of memory cells - each item in the array is stored in its own memory address. 

* Default memory size for an array is 5. 

* The memory size doubles each time the size exceeded. e.g. if the array size is 6 the memory size will be 10 (double 5), or an array size of 21 would have a memory size of 40 (double 20).

* complexity of array methods:

- Read at index - constant
- adding at the end (push) - amortized constant time
- adding in the middle (or beginning) - linear
- deleting in the middle - linear time
- deleting at the end (pop) - constant time

```
  def will_shuffle(array)
    new_array = []
    until array.empty?
      random_index = rand array.length
      new_array << array[random_index]
      array.delete_at(random)
    end
    new_array
  end
```
- the complexity of the above is quadratic. The reason is that the arrau.delete_at(random) changes the make up of the array each time and where it is stored in memory. 

- it can be improved by swapping the item at random index with the last one and using .pop which is done in constant time (rather than delete_at which is linear time). 

- New and better function:
```
def shuffle(array)
    new_array = []
    until array.empty?
      random_index = rand array.length
      new_array << array[random_index]
      array[random_index] array.last
      array.pop
    end
    new_array
  end
```

## Recursion and Memoization (or 'dynamic programming)
* The typical Fibonacci Sequence function is recursive (because it has to go back and calculate all previous fibonacci numbers in the sequence):
```fib(5) = fib(n-1) + fib(n-2)```
* So if you want to check the value of the 5th Fibonacci number, the program will need to check the value of the fib(4) which itself has to check fib(3) and fib(2) which have to themselves check fib(2) and fib(1) and also fib(1) and fib(0) - and this is done again for fib(3). 
* To avoid this you should save the values to memory as you go along
* In pseudo code this might look like this:
```
Fib(n) {
  if n <= 1
    return n
  else if Fn is in memory
    return Fn
  else
    Fn = Rib(n-1) + Fib(n-2)
    return Fn
}
```

