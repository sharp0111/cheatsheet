# First Program:
"Hello World!"
```
$ irb
puts "Hello World"
```
# Runnning a Ruby File
Ruby files have `.rb` file extension\
Create a file - `helloworld.rb`, type in `Hello World` and in the terminal run
```
ruby helloworld.rb
Hello World
```
# Basic Data Types
## Numbers
## Integers
An integer is a sequence of positive whole numbers.
```
12345     # => 12345
1         # => 1
1_000_000 # => 1000000
```
## Floats
There are several ways to write rational numbers in Ruby.
```
1.0         # => 1.0
3.14        # => 3.14
1e12        # => 1000000000000.0
```
## Strings
String objects are created simply using single quotes, ' or double quotes, ".
```
"string value"
'this is also a string value'
```
`#{variable_name}` - to insert a variable or ruby code into a string.\
The Ruby interpreter will attempt to convert the variable’s type to the string's type.
```
x = "Kurt"
"#{x} Cobain played with Nirvana." # => "Kurt Cobain played with Nirvana."
"3*3 is equal to #{3*3}." # => "3*3 is equal to 9."
```
## Arrays
```
[1]                            # => [1]
[1, 2, 3]                      # => [1, 2, 3]
["one", "two", "three"]        # => ["one", "two", "three"]
g = [5, 6, 7]                  # => [5, 6, 7]
g[0]                           # => 5
g[2]                           # => 7
g[3]                           # => nil
```
Nested Arrays:
```
n = [[3, 4], [5, 6, 7], [8, 9, 10, 11]]
n[0]                                         # => [3, 4]
n[2]                                         # => [8, 9, 10, 11]
n[2][3]                                      # => 11
```
Assign a new value to a preexisting array:
```
inception = ["level 1", "level 2", "level 3"]
inception[3] = "limbo"
inception     # => ["level 1", "level 2", "level 3", "limbo"]
```
Overwrite a value in array:
```
g = [5, 6, 7]
g[0] = "zero"
g                # => ["zero", 6, 7]
```
Concatenate two arrays with `+`
```
[3, 4] + [5, 6, 7]     # => [3, 4, 5, 6, 7]
```
## Hashes
A hash has a value for every key. Instantiating a hash is done with squiggly brackets, {}:
```
h = {}
h["Vancouver"] = "British Columbia"
h["Toronto"] = "Ontario"
h["Montreal"] = "Quebec"
h                # => {"Vancouver"=>"British Columbia", "Toronto"=>"Ontario", "Montreal"=>"Quebec"}
h["Montreal"]    # => "Quebec"
```
You can assign an array as a value for a key:
```
starcraft = {}
starcraft["Terran"] = ["Marine", "Medic", "SCV"]
starcraft["Zerg"] = ["Zergling", "Hydrarisk", "Drone"]
starcraft["Protoss"] = ["Zealot", "Dragoon", "Probe"]
starcraft    # =>  => {"Terran"=>["Marine", "Medic", "SCV"], "Zerg"=>["Zergling", "Hydrarisk", "Drone"], "Protoss"=>["Zealot", "Dragoon", "Probe"]}
```
You can assign multiple key-value pairs at the same time:
```
stars = {"Pablo Honey" => 4, "The Bends" => 4.5, "OK Computer" => 5}
```
Since Ruby 1.9, you can also use : to replace =>:
```
more_stars = {"Kid A": 5, "Amnesiac": 4, "Hail to the Cheif": 4, "In Rainbows": 3}
```
## Ranges
A range object has a start value, an ending value and a list of values in between. A range starts with a start value, followed by `..` or `...`, and finishes with an end value.
```
(1..5)  # includes the ending value, 5
(1...5) # does not include the ending value, 5
```
You can use range object on alphabets as well, which makes printing alphabets super easy.
```
("a".."z").each {|x| print x }    # prints abcdefghijklmnopqrstuvwxyz
```
You can even use ranges with the alphabets of other languages. Here is a list of Korean vowels.
```
("ㅏ".."ㅣ").each {|x| print x}  # prints ㅏㅐㅑㅒㅓㅔㅕㅖㅗㅘㅙㅚㅛㅜㅝㅞㅟㅠㅡㅢㅣ
```
## Symbols
Symbols are like string substitutes but they have a few different properties. They are often used in Ruby to avoid computationally expensive string comparisons. Symbols are used usually as keys in hashes. Symbols start with `:` followed by some symbol name.

If you have a code where you are using strings as identifiers for something, consider using symbols instead. For example, if you have two strings, "male" and "female" as identifiers for gender, use :male and :female to identify a person’s gender instead.

You can convert from string to symbol and symbol to string easily using either the `to_sym` to convert from a string to a symbol and `to_s` to convert from a symbol to a string.
```
“string_to_symbol”.to_sym # => :string_to_symbol
“string to symbol”.to_sym # => :”string to symbol”
symbol_to_string.to_s     # => “symbol_to_string”
```
## Boolean
There are only two Boolean values, `true` and `false`. `nil` in Ruby indicates the absence of value. In other programming languages such as JavaScript, `null` is the comparable keyword to `nil` in Ruby.
# Expressions and Statements
## Variables and Constants
Variables are created to store values.
```
a = "a"
a = 1
a = ["cat", "dog"]
```
Variables in Ruby are dynamically typed. As a result, a Ruby variable can store values of different types.

Variables' types:
 - `$`: global variables are available everywhere in a program.
 - `@`: instance variables
 - `@@`: class variables

Constants:\
`THIS_IS_A_CONSTANT`\
Constant in a module: `ModuleName::SOME_CONSTANT`\
Constant in a class: `ClassName::ANOTHER_CONSTANT`\
Assgnment operator: `=`
## Calling Methods
In programming, methods are used to manipulate data.\
In order to call or execute a method, Ruby uses the `.` operator.
* Calling class method: `SomeClass.method_name`
* Calling instance method: `some_instance.method_name`
## Daisy-chain
Ruby allows multiple methods to be called on a method in a sequence.
```
some_method.some_other_method.another_method
```
## Arithmetics
```
5 + 5    # => 10
5 - 5    # => 0
5 * 5    # => 25
5 / 5    # => 1
```
Modulo operator `%`
```
17 % 5     # => 2
```
Exponential operations are done using `**`
```
2 ** 3     # => 8
```
## Boolean Comparisons
Boolean operations are operations that result in either `true` or `false`
* less than `<`
* less than or equal to `<=`
* greater than `>`
* greater than or equal to `>=`
* equal to `==`
* not equal to `!=`
## Boolean Operators
We can incorporate multiple boolean statements with boolean operators
* And: `&&`
* Or: `||`
* Not: `!`
```
((5 > 2) && (4 >= 5)) || (2*3 < 7)    # => true
```
## Conditionals
## If
```
if some_contional_expression
  code_to_execute
end
```
or one liner conditional `if`
```
code_to_execute if some_contional_expression
```
`code_to_execute` will only run if `some_contional_expression` evaluates to `true`
## Else
```
if some_contional_expression
  code_to_execute
else
  some_other_code_to_execute
end
```
one liner
```
some_contional_expression ? code_to_execute_if_true : code_to_execute_if_false
```
## Else if
```
if conditional_a
  run_a
elsif conditional_b
  run_b
elsif conditional_c
  run_c
elsif conditional_d
  run_d
else
  run_anything_else
end
```
## Case
Some large if-elsif-else conditional statements can be simplified
```
# Woody Allen movies
if movie == "Annie Hall"
  4
elsif movie == "Manhatten"
  3.5
elsif movie == "Zelig"
  3
elsif movie == "Midnight in Paris"
  2.5
else
  2
end
```
```
case movie
when "Annie Hall"
  4
when "Manhatten"
  3.5
when "Zelig"
  3
when "Midnight in Paris"
  2.5
else
  2
end
```
## Loops
## While
A `while` loop runs as long as a given condition is true
```
# this loop will run until n reaches 10
n = 0
while n < 10
  puts n
  n += 1
end
```
## For
A `for` loop runs until it reaches a certain condition while performing an action with each iteration
```
for i in 0..9
  puts i
end
```
`while` loops and `for` loops are not commonly used in Ruby. Instead Ruby programmers usually use `to blocks` to handle iterating through enumerable objects
# Error Handling
The `raise` keyword is used to raise an exception and the `rescue` keyword handles an exception
```
def whats_your_age(age)
  raise "wrong argument" if age < 0
  puts "You are #{age}"
end
```
If the exception type is not specified, Ruby treats the exception of `RuntimeError` type.
## Types of Exceptions
* NoMemoryError
* ScriptError
  * LoadError
  * NotImplementedError
  * SyntaxError
* SignalException
  * Interrupt
* StandardError -- default for rescue
  * ArgumentError
  * IndexError
    * StopIteration
  * IOError
    * EOFError
  * LocalJumpError
  * NameError
    * NoMethodError
  * RangeError
    * FloatDomainError
  * RegexpError
  * RuntimeError -- default for raise
  * SecurityError
  * SystemCallError
    * Errno::*
  * SystemStackError
  * ThreadError
  * TypeError
  * ZeroDivisionError
* SystemExit
* fatal – impossible to rescue

It is more suitable to raise the exception as a type of `ArgumentError` instead of `RuntimeError` in the example above. The code below raises a `ArgumentError` exception.
```
def whats_your_age(age)
  raise ArgumentError, "wrong argument" if age < 0
  puts "You are #{age}"
end
```
## Common Usage of `rescue` and `begin`
A `rescue` keyword commonly used with `begin` keyword. A `rescue` keyword appears after lines of code for a `begin` section. If an exception is raised in the `begin` section of the code, the `rescue` section of the code will come to rescue.
```
begin
  # begin section of the code
rescue
  # rescue section of the code
end
```
You can create an exception object and store it in a variable. This exception object will become available in the rescue section of the code. The example below prints the exception message to console.
```
begin
  whats_your_age(-2)
rescue => exception_variable
  puts exception_variable.message
end
```
## `rescue` Based On Exception Type
There are cases where we want to handle different exceptions differently. Ruby allows use of multiple rescue sections to handle exceptions of different types raised in the begin section of the code.

Let's consider the `whats_your_age` method that we wrote earlier.
```
def whats_your_age(age)
  raise ArgumentError, "wrong argument" if age < 0
  puts "You are #{age}"
end
```
This method wasn't written to handle an exception when a string is used as an argument. Let's raise an exception when a string is used as an argument.
```
def whats_your_age(age)
  raise ArgumentError, "wrong argument" if age < 0
  raise TypeError, "wrong type argument" if age.is_a?(String)
  puts "You are #{age}"
end
```
`whats_your_age(-2)` will raise an `ArgumentError` exception and `whats_your_age("minus two")` will raise a `TypeError` exception.

Ruby can handle two different exceptions by creating two `rescue` sections for each exception.
```
begin
  `whats_your_age("minus two")`
rescue ArgumentError => exception_variable
  puts exception_variable.message
  puts "negative number as age?"
rescue TypeError => exception_variable
  puts exception_variable.message
  puts "i can't read english. speak in numbers."
end
```
If you want to handle the rest of the exceptions differently, you can use else.
```
begin
  `whats_your_age("minus two")`
rescue ArgumentError => exception_variable
  puts exception_variable.message
  puts "negative number as age?"
rescue TypeError => exception_variable
  puts exception_variable.message
  puts "i can't read english. speak in numbers."
else
  puts "gotta catch 'em all!"
end
```
If you want to `ensure` that a certain code runs no matter what happens, you can use the `ensure` keyword.
```
begin
  `whats_your_age("minus two")`
rescue ArgumentError => exception_variable
  puts exception_variable.message
  puts "negative number as age?"
rescue TypeError => exception_variable
  puts exception_variable.message
  puts "i can't read english. speak in numbers."
else
  puts "gotta catch 'em all!"
ensure
  puts "this will be printed for sure."
end
```
# Simple Methods
A method is a chunk of code that you can use by invoking its name and appropriate input on an object. The last value evaluated in the method becomes the value of the invoked method. The value of the invoked method is referred to as the return value.
## Defining Methods
A method consists of 4 parts.
```
def method_name(argument1, argument2)
  body_of_code
end
```
1. A `def` keyword that appears at the beginning of every method. An `end` appears at the end of every method.
2. A _method name_ comes right after the `def` keyword.
3. Arguments for a method that will be used to evaluate the return value of the method.
4. The body of code in the method determines the return value of the method.
## Terminating Methods
Methods will terminate when an exception is raised or when a value is returned. Methods can return a value in the middle of the method by using `return` keyword and terminate the method prematurely. Methods don't necessarily need to have a `return` keyword. When methods don't have a `return` keyword, they will run until the end of the body of the method. The value evaluated in the method will become the return value of the method.
```
def arithmatic_sum(n)
  if n < 0
    raise ArgumentError, "argument must be greater than 0."
  elsif !n.is_a?(Integer)
    raise TypeError, "argument must be an integer"
  else
    n*(n+1)/2
  end
end
```
In `arthmatic_sum` method, we see three ways in which the method can end.
1. If the method takes a negative number as the method's argument, the method raises an ArgumentError exception and terminates the method.
2. If the method takes a non-integer number as the method's argument, the method raises a TypeError exception and terminates the method.
3. If the argument is a positive integer, the method will evaluate `n*(n+1)/2` and return the value.
## Method Invocations
Methods are always called on an object.
```
x = 2
x.minus(2) #=> 0

def minus(n)
  self - n
end
```
`self` refers to the object that method is invoked on. In this case, `self` refers to `x`.
A typical method invocation consists of 3 parts.
```
some_object.method_name(argument)
```
1. An object on which the method is called on.
2. `.` which demarcates the object and the method name
3. The method with its name and appropriate arguments
## Conventions Around Ruby Methods
Although many of these rules are not explicitly enforced by the Ruby interpreter, programmers themselves have developed programming conventions regarding how Ruby methods are named.
* All alphabets are lower case.
```
def lowercased_method_name
end
```
* !Use _camel case_ to indicate multiple number of words in the method name.
```
# use this
def something_with_multiple_words
end

# rather than this
def somethingWithMultipleWords
end
```
* Method names that end with `=` are _setter_ methods. Setter methods are often used to set the value of an object or an attribute of an object.
```
def set_height_in_cm=(value)
  self.height_in_cm = "#{value} cm"
end
```
* Method names that end with `?` are methods that have a boolean return value.
```
def did_you_pass?(average)
  average > 59.5
end
```
* Method names that end with a `!` are mutators. Mutators alter the object that the method is called on. In the example below, notice how `sort` doesn't alter `a`, but calling `sort!` does alter `a`.
```
a = [7, 3, 5, 4, 9, 8, 1, 6, 2, 0]
a.sort     # => [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
a          # => [7, 3, 5, 4, 9, 8, 1, 6, 2, 0]
a.sort!    # => [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
a          # => [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```
* Ruby operators such as `*`, `-`, and `+` can also be used as method names. These are called `operator methods`.
```
def +(points)
  self.score += points
end

def -(points)
  self.score -= points
end
```
* Parentheses are optional when methods are called. However, parentheses must be used when method invocation becomes ambiguous.
```
# both are allowed
puts arithmatic_sum(10) # preferred
puts arithmatic_sum 10
```
## Method Arguments
## Defalt values
Ruby allows you to have variables with a default value. If the method is called without setting a value in the default value parameter, the default value is used. If the method is called with a new value in the default value parameter, the variable is assigned the new value instead of the default value.
```
def male_title(name, prefix = "Mr.")
  prefix + ' ' + name
end

male_title("Malkovich")  # => "Mr. Malkovich"

male_title("Who", "Dr.") # => "Dr. Who"
```
## Dealing With A Varying Number of Arguments For A Method
Some methods may not have a definitive number of arguments. To deal with this, use a `*` operator in front of the argument name, when you define a method. This denotes that the method may take a varying number of arguments.
```
def connect(first, *rest)
  first + rest.join('')
end

connect("a")                        # => "a"
connect("a", "b")                   # => "ab"
connect("a", "b", "c", "d", "e")    # => "abcde"
```
If the argument name doesn't start with an `*`, that means that you must insert a value for that argument when you call the method.
```
connect    # ArgumentError: wrong number of arguments (0 for 1+)
```
You can pass an array into methods that have an `*` before the variable name in the paramter.
```
array = ["a", "b", "c", "d", "e"]
connect(*array)    #=> "abcde"
```
Note that `connect(array)` and `connect(*array)` are not the same. The `connect(array)` case considers `first = array` and `rest = nil`. `connect(*array)` case considers `first = "a"` and `rest = ["b", "c", "d", "e"]`.
## Hashes As Arguments
As the number of arguments for a method increases, it becomes more difficult to remember the order of the arguments when you call the method. You may use hashes as arguments for methods. This avoids the need for remembering the exact order of methods' arguments.
```
def allow_hash(hash)
  hash[:a] + hash[:b]
end

allow_hash({:a => 1, :b => 2})      # => 3
```
You can omit `{}` surrounding the keys and values for the hash argument if the hash is the last argument of the method.
```
allow_hash(:a => 1, :b => 2)        # => 3
```
# Iterators
If you have anything you need to iterate multiple times in Ruby, consider using iterators first. Iterators are so commonly used in Ruby that, while and for which frequently appear in C, C++ and Java code for iterations are almost never used in Ruby.
## Iterators In Action
```
# NASA countdown
10.downto(0) do |k|
  if k != 0
    puts k
  else
    puts "0\nLift off!"
  end
end
```
This code will print the following in the console.
```
10
9
8
7
6
5
4
3
2
1
0
Lift off!
```
`downto` is a iterator method that is applied to `10` and accepts `0` as an argument. The iterator is followed by a chunk of code called _block_. The code inside the block is evaluated at each iteration.\
More examples:
```
3.times {|t| puts "Three times the charm" }

members = ["Adam", "Bob", "Claire"]
# Greet members
members.each {|member| puts "Hello #{member}" }

# Get the length of the member's name
members.map {|member| member.length } # => [4, 3, 6]
```
## Iterator-Block Combination
```
object_to_iterate.iterator_method(arguments) do |parameter1, parameter2|
  # body of block
end
```
1. Iterator methods and blocks go hand in hand. A block appears after an iterator method.
2. An object to iterate (`object_to_iterate`) is always stated before an iterator method (`iterator_method`).
3. Iterator methods may or may not have arguments.
4. Blocks start with `do` and end with `end`. If the iterator-block code is written in a single line, you should use `{` and `}` by convention.
5. Blocks may contain parameters like methods.
6. The body of block is evaluated in every iteration.
## Common Iterators
## `each`
Executes block and returns the list of objects without mutating
* prints 246810 and returns 1, 2, 3, 4, 5
```
[1, 2, 3, 4, 5].each {|x| print x*2 }
```
* prints artists’ name and their nationality and returns the hash itself
```
celebs = {"Justin Bieber" => "Canadian",
  "Psy" => "Korean",
  "Nicki Minaj" => "American"}
celebs.each {|key, value| puts "#{key}: #{value}" }
```
## `each_with_index`
Almost like `for` loop with index. The index begins from 0.
* prints table of contents to the console.
```
contents = ["Overview",
  "Basic Data Types",
  "Expressions and Statements",
  "Error Handling",
  "Simple Methods",
  "Iterators",
  "Classes",
  "Test Driven Development with RSpec",
  "Sinatra Web Development"]

contents.each_with_index do |content, index|
  puts "#{index+1}. #{content}"
end
```
## `map`
Executes block and returns the list of mutated objects
* returns 2, 4, 6, 8, 10
```
[1, 2, 3, 4, 5].map {|x| x*2 }
```
## `select`
Returns a list of objects when condition is true
* returns 2
```
[1, 2, 3, 4, 5].select {|x| x==2 }
```
## `reject`
Returns a list of objects when condition is false
* returns 1, 3, 4, 5
```
[1, 2, 3, 4, 5].reject {|x| x==2 }
```
## `partition`
Create two collections. First collection for true, second for false.
* returns 4, 5, 1, 6
```
[1, 4, 5, 6].partition {|x| x==4 || x==5 }
```
## `upto`
Numeric iterator that increases index by one each iteration.
* determine arithmetic sum
```
sum = 0
0.upto(100) {|index| sum += index }
sum # => 5050
```
## `downto`
Numeric iterator that decreases index by one each iteration.
* countdown
```
10.downto(0) {|index| puts index }
```
## `times`
Numeric iterator that iterates a given number of times.
* print "something" 5 times
```
5.times {|x| puts "something" }
```
## `inject`
Has two block parameters. First parameter contains the accumulated value from the previous iteration.
* arithmetic sum 2
```
one_to_ten = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
sum = one_to_ten.inject do |sum, element|
  sum += element
end
sum # => 55
```
* arithmetic sum 3 using an argument on inject
```
one_to_ten = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
sum2 = one_to_ten.inject(10) do |sum, element|
  sum += element
end
sum2 # => 65, 10 is added
```
## Custom Iterators
We can create custom iterators by using a `yield` statement. `yield` lends the value to the block.
```
class Integer
  def get_randoms_in(max)
    self.times {|x| yield rand(max) }
  end
end

#
5.get_randoms_in(10) {|x| puts x }
```
The code above prints the following:
```
9
6
4
4
6
```
`get_randoms_in` is a custom iterator. The method uses an iterator, `times`. During each iteration, the `yield` statement lends the evaluated value from `rand(max)` to the block that comes after `get_randoms_in`. The `rand(max)` code returns a random integer between 0 and `max`. In the block that comes after `get_randoms_in`, the random number is printed to console.

We have the `get_randoms_in` method wrapped in an `Integer` class. This is because we wanted to call `get_randoms_in` method on an integer object such as `5`.
# Classes
Object oriented programming (OOP) is a programming style that roughly revolves around manipulating abstraction called objects.

_Classes_ are abstractions of common objects. _Objects_ refer to specific instances of classes.

A class may have _attributes_. Attributes are common characteristics of instances of a class.

A class may have _methods_. Methods are associated with actions done by objects.
## Creating A Class
Use `class` keyword to create classes in Ruby.
```
class Car
end
```
The class name must start with a capital letter. `self` refers to the class, if `self` is mentioned in the body of a class, but it is not referring to the instance methods in the class.
## Instantiation and Initialization
_Instantiation_ is creating an object of a certain _type_ from a class. The class is what determines the type of an object. For example, A _Civic_ is a _Car_ typed object created through _instantiation_ from the _Car_ class.

_Initialization_ is the process that gives values to attributes of an instantiated object. It could be said that a Civic has 1800 cc for the engine attribute and 140 for the horse power attribute.

Instantiation is done with the class method called `initialize`. But here is the confusing part. When you want to invoke the `initialize` method, you invoke it by calling `new` instead. Normally, when you invoke a method, you call it with the same method's name. To make the confusion even worse, you don't need to explicitly write an `initialize` method in the class to invoke it using `new`. The code below will run without any error.
```
class Car
end

my_new_car = Car.new
```
Initialization of an object may or may not happen during the instantiation. If the initialization of an object is done during instantiation, the attributes are initialized with some value by passing arguments to the `new` method. Initialization through instantiation requires you to write an `initialize` method in the class. You also need to write methods for the attributes of the class.
## Attributes
Attributes are relevant qualities that describe a class.
```
class Car
  attr_accessor :manufacturer, :car_name, :engine, :horse_power
end
```
`attr_accessor` is a method that defines the attributes of this class. We created attributes called _manufacturer_, _car_name_, _engine_, and _horse_power_. By creating attributes with `attr_accessor`, you can set values to attributes and get values from attributes.
```
class Car
  attr_accessor :manufacturer, :car_name, :engine, :horse_power
end

# instantiation
civic = Car.new

# setting values to attributes
civic.car_name = "Civic"
civic.manufacturer = "Honda"
civic.engine = 1800
civic.horse_power = 140

# getting values from attributes
puts civic.car_name
puts civic.manufacturer
puts civic.engine
puts civic.horse_power
```
The `attr_accessor` method is actually a shorter way of writing setter and getter methods. The example above could've been written with many more setter and getter methods like below.
```
class Car
  #setters
  def manufacturer=(value)
    @manufacturer = value
  end

  def car_name=(value)
    @car_name = value
  end

  def engine=(value)
    @engine = value
  end

  def horse_power=(value)
    @horse_power = value
  end

  #getters
  def manufacturer
    @manufacturer
  end

  def car_name
    @car_name
  end

  def engine
    @engine
  end

  def horse_power
    @horse_power
  end
end

# instantiation
civic = Car.new

# setting values to attributes
civic.car_name = "Civic"
civic.manufacturer = "Honda"
civic.engine = 1800
civic.horse_power = 140

# getting values from attributes
puts civic.car_name
puts civic.manufacturer
puts civic.engine
puts civic.horse_power
```
Attributes are just methods that assign values to class variables and get values of class variables. Class variables are the variables that start with `@`. Don't write setters and getters unless you feel that there is a compelling reason to do so. Simply use the `attr_accessor` method to write attributes for a class.

Setting the values of attributes one by one can be tedious when a class has many attributes. In such cases, you can write the `initialize` method that takes a hash of attributes and values as arguments.
```
class Car
  attr_accessor :manufacturer, :car_name, :engine, :horse_power

  def initialize(hash)
    @manufacturer = hash[:manufacturer]
    @car_name = hash[:car_name]
    @engine = hash[:engine]
    @horse_power = hash[:horse_power]
  end
end

civic = Car.new({
  :manufacturer => "Honda",
  :car_name => "Civic",
  :engine => "1800",
  :horse_power => "140"
})

puts civic.car_name
puts civic.manufacturer
puts civic.engine
puts civic.horse_power
```
## Methods in Classes
Classes have methods. Some methods for a class exist simply by creating a class. For example, the class method `name` exists for all classes even though you don't explicitly write the method.
```
class Car
end

Car.name
```
There is actually a class method that returns an array of class methods available to the class by simply being created.
```
class Car
end

Car.methods
```
A class can contain two kinds of methods. They are instance methods and class methods. Instance methods for a class are applied to instances of the same type. Class methods are applied to its class.
## Instance Methods
Instance methods are methods that are invoked for instances of the class. Like other methods, the method is applied with the `.` operator.
```
class Car
  attr_accessor :manufacturer, :car_name, :engine, :horse_power

  def initialize(hash)
    @manufacturer = hash[:manufacturer]
    @car_name = hash[:car_name]
    @engine = hash[:engine]
    @horse_power = hash[:horse_power]
  end

  def to_print
    puts "Manufacturer: #{self.manufacturer}"
    puts "Name: #{self.car_name}"
    puts "Engine: #{self.engine}"
    puts "Horse pwer: #{self.horse_power}"
  end
end

civic = Car.new({
  :manufacturer => "Honda",
  :car_name => "Civic",
  :engine => "1800",
  :horse_power => "140"
})

civic.to_print
```
The Car class contains a `to_print` method. The `to_print` method is an instance method that Car objects can use to print values of attributes. To use the `to_print` method, we prepare a Car object, `civic`. Then we apply the `to_print` method onto `civic` with the `.` operator. As a result, the `to_print` method prints the attributes of `civic`.
## `self`
1. `self` refers to the object that the method is invoked on. The object here may refer to an object instance, a class, or a module and return value of a method.

     The `to_print` method makes use of `self` to refer to the object the method is invoked on. In this case, `self` refers to `civic` in this case.
2. `self` can also be used to denote that a method contained in a class is a _class method_.
## Class Methods
Class methods are methods that are called onto classes. The `.` operator is used to invoke the method on the class like other methods.

Class methods are defined in a class with `self`. Class methods take the form of `self.method_name`.
```
class Car
  def self.manufacturer_list
    %w{Audi BMW Buick Cadillac Chevrolet Chrysler Dodge Ferrari
       Ford GM GEM GMC Honda Hummer Hyundai Infiniti Isuzu Jaguar
       Jeep Kia Lamborghini Land Rover Lexus Lincoln Lotus Mazda
       Mercedes-Benz Mercury Mitsubishi Nissan Oldsmobile Peugeot
       Pontiac Porsche Regal Saab Saturn Subaru Suzuki Toyota
       Volkswagen Volvo}
  end
end

Car.manufacturer_list
```
The `manufacturer_list` method is a class method that returns an array of car manufacturers. The method is called stating the class `Car` and then using the operator `.`.

`%w{words}` returns an array of strings for words split by a space.
## Inheritance
Classes can have relationships with other classes. Say we had a Sedan class.
```
class Sedan
end
```
Sedans are a subset of cars. Therefore, when we relate the Car class and the Sedan class, we say, "Sedan class _inherits from_ Car class" or "Sedan class _extends_ Car class". The Car class is a _superclass_ or a _parent class_ and the Sedan class is a _subclass_ or a _child class_.

A class may have many subclasses, but it can only belong to superclass. _Descendants_ of a superclass are subclasses that are _children_ to the superclass. _Ancestors_ of a subclass are any classes that have the subclass as a child.
```
class Car
end

class Sedan < Car
end
```
## Methods in Superclasses and Subclasses
A subclass inherits methods from its superclass.
```
class Car
  def vroom
    "vroom vroom"
  end
end

class Sedan < Car
end

civic = Sedan.new
civic.vroom
```
Notice that Sedan class doesn't have a method called `vroom` in the example above. However, the Sedan object, `civic` still is able to invoke the `vroom` method because the Sedan class inherits from the Car class. As a result `civic.vroom` returns "vroom vroom".

What happens if the Sedan class also has a method called `vroom`, but does something different?
```
class Car
  def vroom
    "vroom vroom"
  end
end

class Sedan < Car
  def vroom
    "vvvvrooom vroom vroom"
  end
end

civic = Sedan.new
civic.vroom
```
Because `civic` is a Sedan object, it looks for the instance method in the Sedan class first-before any superclass. The Sedan class has an instance method called `vroom`, so `civic.vroom` returns `"vvvvrooom vroom vroom"`. When a subclass's method name is same as its superclass's method, the subclass's method is said to _override_ the superclass's method.
## Method Availability
Instance methods are either _public_, _private_, or _protected_. The three kinds of methods define the availability of methods in the program.

Methods are public by default. When a method is public, it can be used outside the class freely.
```
class Car
  def vroom
    "vroom vroom"
  end
end

class Unrelated
  def car_vroom
    car = Car.new
    car.vroom
  end
end

unrelated = Unrelated.new
unrelated.car_vroom
```
We have a class called Unrelated that is entirely unrelated to the Car class. Yet because `vroom` method in the Car class is public, it can be used inside another class's method. In this case, the `car_vroom` method inside Unrelated is freely using `vroom` method of Car class.

_Private methods_ are only available to other instance methods in the class and instance methods in the subclasses.

_Protected methods_ are available to other instance methods in the class and instance methods in the subclasses too-like private methods.

The difference between protected methods and private methods is the object that the instance methods are invoked on. Private instance methods are invoked implicitly on the `self`. Protected instance methods are invoked on any instance of the class.
```
class Car
  protected
    def crunk
      "crunk"
    end
end

class Sedan < Car
  def car_crunk
    car = Car.new
    car.crunk
  end

  def sedan_crunk
    self.crunk
  end
end

class Unrelated
  def car_crunk
    car = Car.new
    car.crunk
  end
end

car = Car.new
car.crunk # NoMethodError: protected method `crunk' called for ...

sedan = Sedan.new
sedan.car_crunk
sedan.sedan_crunk

unrelated = Unrelated.new
unrelated.car_crunk # NoMethodError: protected method `crunk' called for ...
```
The example above illustrates the available scope of protected method. First, the car instance outside the class cannot call `crunk` because it's a protected method. However, you can call the `crunk` method on the car instance, when the instance is inside the Sedan class because the Sedan class is a subclass of the Car class. Lastly the unrelated instance cannot make use of the `crunk` method because the Unrelated class does not inherit it from the Car class.
```
class Car
  private
    def flunk
      "flunk"
    end
end

class Sedan < Car
  def car_flunk
    car = Car.new
    car.flunk
  end

  def sedan_flunk
    self.flunk
  end
end

class Unrelated
  def car_flunk
    car = Car.new
    car.flunk
  end
end

car = Car.new
car.flunk # NoMethodError: private method `flunk' called for ...

sedan = Sedan.new
sedan.car_flunk # NoMethodError: private method `flunk' called for ...
sedan.sedan_flunk # NoMethodError: private method `flunk' called for ...

unrelated = Unrelated.new
unrelated.car_flunk # NoMethodError: private method `flunk' called for
```
The code above illustrates the private method availability in different cases. Notice that whenever the private method, `crunk` was used outside the class itself, and the subclass, Sedan, a NoMethodError was thrown.

As a rule of thumb, public methods are written first in the class, then comes protected methods followed finally by the private methods inside a class.
```
class Car
  #public methods

  #protected methods
  protected

  #private methods
  private
end
```
## Modules
Modules are like classes except for the fact that modules cannot create objects through instantiation whereas classes can. Modules also lack the ability to inherit from or inherit to other modules unlike classes. Modules are written with a keyword, `module`. And the module name followed by the keyword `module` must start with a capital letter.
```
module Human
end
```
Modules are used as a namespace for related methods and classes.
```
module Human
  # using self
  def self.genders
    ["male", "female"]
  end

  # using moduel name
  def Human.ubermensch
    "programmers"
  end

  class Male
    def origin
      "Mars"
    end
  end

  class Female
    def origin
      "Venus"
    end
  end
end

Human.genders
Human.ubermensch
man = Male.new  # this will not work
woman = Female.new  # this will not work either

man = Human::Male.new
woman = Human::Female.new
man.origin
woman.origin
```
Modules have module methods that are similar to the way class methods work. Module methods are written by prefixing `self` or the module name `ModuleName`. There is no difference between the two ways of writing the module methods.

When you refer to a class inside a module, you must prefix it with the `ModuleName` and double colons `::`.
# References
1. [http://jasonkim.ca/projects/just_enough_ruby_to_get_by/](http://jasonkim.ca/projects/just_enough_ruby_to_get_by/)
