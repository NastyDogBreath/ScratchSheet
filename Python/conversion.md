# Python 3 Cheatsheet

## Base Types

`int 783 0 -192 0b010 0c642 0xF3`

`float 9.23 0.0 -1.7e-6`

`bool true false`

`str "Hello" "Line1\nLine2" "I\'m'" """X\tY\yZ1\t2\t3"""`

`bytes b"toto\xfe\775`

## Blocks
### editor should be configured to 4 spaces as a tab

> statement1:

>     code

## Boolean Logic

These are the same as C#, except using _**True**_ and _**False**_ instead of lowercase

`a and b`

`a or b`

`a <= b`

`not a`

`return a or b`

## Conditional Statements

`if bool(x)==True:`

`if x`

`if not x`

`if num<100:`

`elif:`

`else:`

## Container Types

`list [1,5,9]  ["x",11,8.4] ["abc"]`

`tuple(1,5,9) 11,"y",4.3 ("abc",)   => Non modifyable`

`str bytes => Non modifyable`

`dict {key:value}    dict(a=1,b=7,k="z")   {1:"one",3:"three",2:"two",3.14:"π"}`

`set {"key1, "key2"}  {1,5,8,5}`

`frozenset {1,2,3,4} => immutable set`



### Operations (Dictionary)

`d[key] => value`

`d.clear()`

`del d[key]`

`d.update(d2)`

`d.keys()`

`d.values()`

`d.items()`

`d.pop(key[,default])`

`d.popitem() => (key, value)`

`d.get(key[,default]) => value`

`d.setdefault(key[,default]) => value`

### Operations (List)

`lst.append(val)`

`lst.extend(seq) (add a collection at the end)`

`lst.insert(index,val)`

`lst.remove(val) (removes the first item with that value)`

`lst.pop([inx]) => value  (removes and returns value)`

`lst.sort()`

`lst.reverse()`

### Operations (Set)

`| => union`

`& => intersection`

`- ^ => difference/symmetric dif`

## Conversion
`int("15") => 15`

`int("3f", 16) => 63 (can specify number base in 2nd parameter)`

`int(15.56) => 15 (truncates decimal)`

`float("-11.24e8") => -1124000000.0`

`bool(x) => false (null or empty)`

`str(x) => "..."`

`chr(64) => '@'`

`ord('@') => 64`

`repr(x) => "..." (literal representation)`

`bytes[72,9,64] => b'H\t@'`

`list("abc") => ['a','b','c']`

`dict([(3,"three"), (1, "one")]) => {1:'one',3:'three'}`

## Exception Handling
### use finally in all cases

`try:`

`except Exception as e:`

`finally:`

`raise ExceptionClass(...)`

## Handling Files
`f = open("myfile.txt,"w",encoding="utf8")`

### reading
`f.read([n]) => next chars (if not specified, read to the end)`

`f.readlines([n])`

`f.readline()`

`f.write("foo)`

`f.writeline(list)`

`f.close()`

`f.flush() => write cache`

`f.truncate([size])`

`f.tell() => position`

`f.seek(position[,origin])`

`with open(...) as f: for line in f:  #process of each line`


## Function Decloration

`def myfunction(x,y,z):`

`def myfunction(x,y,*tuple, z=False, **dict):`

`return result`

`return None`

### call a function

`a = myfunction(4, 1%3, 5**2)`

## Identifiers
### language keywords forbidden

### case sensitive

`a...zA...Z_0...9`

## Imports

### modules and packages searched in python path (cs sys.path)

`from somemod import mod1,mod2 as somemodname`

`import somemod => (somemod.mod1)`

## Loops

`for a in b:`

`for ind in range(len(lst)):`

`for ind,val in enumerate(lst):`

`while logic_condition:`

`while i < 100:`


### controls

`break => immediate exit`

`continue => next iteration`

`else => block for normal loop exit`

## Math

### typical operators

`+ - *  /`

`// => div`

`% => mod`

`** => squared`

`(1+5.3)*2 => 12.6`

`abs(-3.6) => 3.6`

`pow(4,3) => 64`

`round(15.56, 1) => 15.6`

### modules

`from math import sin,cos,pi,sqrt,log,ceil,floor,random,fractions`

`sin(pi/4) => 0.707...`

`cos(2*pi/3) => -0.4999...`

`sqrt(9) => 3`

`ceil(5.5) => 6`

`floor(5.5) => 5`

## Operations

`len(x) => items count`

`min(x)  max(x)  sum(x)`

`val in x`

`val not in x`

`all(x) => true if all`

`any(x) => true if at least one`

### ordered sequences

`reversed(x) => inversed iterator`

`x.index(val) => position`

`x+x2 => concatenate`

`x.count(val) => gets the count of occurances of val`

`x*5 => duplicate  (not sure what this is yet)`

### copying
`import copy`

`copy.copy(x)`

`copy.deepcopy(x)`

## Sequences

`lst=[1,2,3,4,5,6,7,8,9,10]`

### syntax (0 based indexing)

`len(lst) => 10`

`lst[start:end:step]`

`lst[0] => 1`

`lst[9] => 10`

`lst[-1] => 10`

`lst[-5] => 6`

`lst[:-1] => [1,2,3,4,5,6,7,8,9]`

`lst[1,-1] => [2,3,4,5,6,7,8,9]`

`lst[::-1] => [10,9,8,7,6,5,4,3,2,1]`

`lst[:] => [1,2,3,4,5,6,7,8,9,10]  (shallow copy)`

### integer sequences 

`range([start,] end [,step])`

`range(5) => gets items from index 0 to 4`

`range(len(seq)) => sequence of index of values in seq`

### missing slice indications

`del lst[3:5]`

`lst[1:4] = [2,3]`

## String Operations

`s.startswith(prefix[,start[,end]])`

`s.endswith(suffix[,start[,end]])`

`s.strip([chars])`

`s.count(sub[,start[,end]])`

`s.lower()  s.upper()   s.title()  s.swapcase()`

`s.casefold()  s.capitalize()`

`s.ljust([width,full]) s.center([width,fill]) s.rjust([width,full])`

`s.encode(encoding)  s.split([sep])   s.join(seq)`

`s.is...()   s.isalpha()`

## Variable Assignment
`x=1.2+8+sin(y)`

`a=b=c=0 (assignment to the same value)`

`a,b,c=6,4.3,0 (assignment to multiple variables)`

`a,b=b,a (values swapping)`

`a,*b=seq *a,b=seq  (unpacking of a sequence in item and list)`

`a+=3 g-=5 (these are the same as javascript/c#)`

`x=None (undefined)`

`del x (remove name x)`
