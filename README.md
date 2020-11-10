# TDD Test Driven Development

### Type of testing
```
- unit testing
- TDD
- Python has several modules that we can use
```
### To test our code
```
- pytest
- unittest
```

### Why TDD

- TDD helps us minimise the risk of failure before sending the product to production
steps
```
- we will create a file to write our tests
- we will run the test they will all fail
- we will create a file to write our code
- we will refactor and add the code to pass the tests
```
### Naming convention - Important
```
code file: simple_calc
test file: test_simple_calc
```

#### Example

- Install the required frameworks pip install pytest
- We then write the test_simple_calc file first:
```
    # Write a class to write our tests
    class CalcTest(unittest.TestCase):
    # Create an object of the class we are testing
    calc = SimpleCalc()

    # IMPORTANT - Must use the 'test' word in our methods

    # We are asking python to test if 2 + 4 = 6
    def test_add(self):
        self.assertEqual(self.calc.add(2, 4), 6)

    # Test if 4 - 2 =2
    def test_subtract(self):
        self.assertEqual(self.calc.subtract(4, 2), 2)

    # Test if 2 x 2 = 4
    def test_multiply(self):
        self.assertEqual(self.calc.multiply(2, 2), 4)

    # Test if 6 / 3 = 2
    def test_divide(self):
        self.assertEqual(self.calc.divide(6, 3), 2)
```
### We can use two testing commands:
1. python -m unittest or python -m unittest discover -v
2. python -m pytest or pytest or pytest -v

- We then write the actual code based on fixing these errors. So let's create the simple_calc file:
```
    # This file contains functional code to pass the test
class SimpleCalc:
   
   def add(self, num1, num2):
       return num1 + num2

   
   def subtract(self, num1, num2):
       return num1 - num2
   
   
   def multiply(self, num1, num2):
       return num1 * num2
   
   
   def divide(self, num1, num2):
       return num1 / num2
       
```
#### This is after creating all required functionalities to PASS the test file


### What's Important?

- When writing the test class, you must inherit unittest.TestCase
- The methods in the test class must start with test_
- Choose correct assert methods based on what you want (possible asserts are at the bottom of the page)
class Test(unittest.TestCase):
```
    def test_case1(self):
```

### Other Notes

The TestCase class provides several assert methods to check for and report failures. The following table lists the most commonly used emthods(see assert.png for a list)
