🐍 Python CheatsheetBasic Syntax & VariablesExecution: Save as .py file and run in terminal: python your_file.pyComments:Single line: # This is a commentMulti-line: """This is a multi-line comment"""Print Output: print("Hello, World!")User Input: name = input("Enter your name: ") (Returns a string)Variable Assignment:Pythonx = 10         # Integer
pi = 3.14      # Float
greeting = "Hi" # String
is_true = True # Boolean (True or False)
Data Types (Containers)TypeSyntaxDescription & PropertiesMethods (Examples)List[1, "two", 3.0]Mutable, ordered sequence, supports heterogeneous types.list.append(item), list.pop(), list.remove(item), list.sort(), list[index:slice]Tuple(1, "two", 3.0)Immutable, ordered sequence. Faster than lists.tuple.index(item), tuple.count(item), tuple[index:slice]Set{1, 2, 3} or set()Mutable, unordered collection of unique items.set.add(item), set.remove(item), set1.union(set2), set1.intersection(set2)Dictionary (Dict){'key': 'value', 2: 'two'}Mutable, unordered collection of key-value pairs. Keys must be immutable and unique.dict['key'], dict.keys(), dict.values(), dict.items(), dict.get('key', default)String (Str)"Hello" or 'World'Immutable sequence of characters.str.upper(), str.lower(), str.strip(), str.split(sep), str.join(list)Indexing & SlicingFor Lists, Tuples, and Strings:Access element: my_list[0] (First element)Last element: my_list[-1]Slice: my_list[start:end:step]my_list[1:4] (Elements at index 1, 2, 3)my_list[:3] (From start up to index 2)my_list[2:] (From index 2 to end)my_list[::-1] (Reverse the sequence)Operators & Boolean LogicTypeOperatorExampleDescriptionArithmetic+, -, *, /a + bAddition, Subtraction, Multiplication, Division//10 // 3 == 3Floor Division (integer result)%10 % 3 == 1Modulo (remainder)**2 ** 3 == 8ExponentiationComparison==, !=, >, <, >=, <=a == bEqual, Not Equal, Greater/Less Than/EqualLogicaland, or, notx > 5 and y < 10Standard Boolean logicMembershipin, not in'a' in my_listChecks if element is present in a collection.Identityis, is nota is bChecks if two variables refer to the exact same object in memory.Control FlowConditionalsPythonif condition1:
    # Code block 1
elif condition2:
    # Code block 2
else:
    # Code block 3
LoopsFor Loop (Iteration):Python# Iterate over a list/tuple/string/dict keys
for item in my_collection:
    print(item)

# Iterate a specific number of times
for i in range(5):  # 0, 1, 2, 3, 4
    print(i)

# Iterate with index
for index, item in enumerate(my_list):
    print(f"Index {index}: {item}")
While Loop (Condition-based):Pythoncount = 0
while count < 5:
    print(count)
    count += 1
Loop Control:break: Terminates the current loop.continue: Skips the rest of the current iteration and moves to the next.FunctionsDefinition:Pythondef my_function(param1, param2=10):
    """This is a docstring explaining the function."""
    result = param1 + param2
    return result

# Call the function
output = my_function(5)
output_kw = my_function(param1=5, param2=2)
Arbitrary Arguments:Pythondef sum_all(*args):
    # args is a tuple of positional arguments
    return sum(args)

def print_info(**kwargs):
    # kwargs is a dictionary of keyword arguments
    for key, value in kwargs.items():
        print(f"{key}: {value}")
Lambda Functions (Anonymous):Pythonadd = lambda a, b: a + b
print(add(2, 3)) # Output: 5
Classes & Object-Oriented Programming (OOP)Pythonclass Dog:
    # Class attribute
    species = "Canis familiaris"

    # Constructor method
    def __init__(self, name, age):
        # Instance attributes
        self.name = name
        self.age = age

    # Instance method
    def bark(self):
        return f"{self.name} says Woof!"

# Create an object (instance)
my_dog = Dog("Buddy", 5)
print(my_dog.name) # Output: Buddy
print(my_dog.bark()) # Output: Buddy says Woof!

# Inheritance
class Poodle(Dog):
    def bark(self):
        # Override the parent method
        return f"{self.name} says Yelp!"
Exception HandlingPythontry:
    # Code that might raise an exception
    result = 10 / 0
except ZeroDivisionError:
    # Handle a specific exception
    print("Cannot divide by zero!")
except Exception as e:
    # Handle any other exception
    print(f"An unexpected error occurred: {e}")
else:
    # Executes only if the 'try' block succeeds (no exception)
    print("Division was successful.")
finally:
    # Executes always, regardless of an exception
    print("Execution finished.")
List Comprehensions (Concise Iteration)Basic: [expression for item in iterable]Example: squares = [x * x for x in range(10)]With Condition: [expression for item in iterable if condition]Example: evens = [x for x in range(10) if x % 2 == 0]Dictionary Comprehension: squares_dict = {x: x*x for x in range(5)}File OperationsPython# Reading a file
with open('data.txt', 'r') as f:
    content = f.read()     # Read all content
    lines = f.readlines()  # Read content line by line into a list

# Writing to a file (w: overwrite, a: append)
with open('output.txt', 'w') as f:
    f.write("Hello Python!\n")
    f.writelines(['line1\n', 'line2\n'])
