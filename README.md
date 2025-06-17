# Programming Answers

# **NEW QUESTIONS**

# 31. Square Even Numbers
```python
def squareEvenNumbers(arr):
    return [x**2 for x in arr if x % 2 == 0]
```

# 32. Extract First Letters
```python
def extractFirstLetters(arr):
    return [x[1] for x in arr if len(x) > 3]
```

# 33. Filter and Format Prices
```python
def filterAndFormatPrices(arr):
    return [f'Product: {x[0]}, Price: ${x[1]}' for x in arr if x[1] > 10]
```

# 34. Simple Calculator
```python
class SimpleCalculator:
    def __init__(self):
        self.__result = 0
    
    def add(self, num):
        self.__result += num
    
    def subtract(self, num):
        self.__result -= num
    
    def get_result(self):
        return self.__result

calc = SimpleCalculator()
calc.add(15)
calc.subtract(10)
print(calc.get_result())
```

# 35. Student Information
```python
class StudentInformation:
    def __init__(self, name: str, age: int, grades: list):
        self.name, self.age, self.grades = name, age, grades
    
    def average_grade(self):
        return round(sum(self.grades) / len(self.grades), 2) if self.grades else 0

student = StudentInformation(name='Goofy', age=18, grades=[80, 75, 90])
print(student.average_grade())
```

# 36. Rectangle Area and Perimeter
```python
class Rectangle:
    def __init__(self, width, height):
        self.width = width
        self.height = height
    
    def area(self):
        return self.width * self.height
    
    def perimeter(self):
        return 2 * (self.width + self.height)
    
rect = Rectangle(2, 5)
print(rect.area())
print(rect.perimeter())
```

# 37. Factorial Calculation (with loop)
```python
def calculate_factorial(n):
    if n == 0: return 1
    result = n
    for i in range(n-1, 1, -1):
        result *= i
    return result
```

# 54. Safe Integer Conversion
```python
def safe_int_conversion(value):
    try:
        return int(value)
    except ValueError:
        return None
```

# 1. Sum of all digits
```python
def sumDigits(s):
	result = 0
	for i in s:
		result += int(i)
	return result
```

# 2. Find Factorial
```python
def factorial(n):
	if n <= 1:
		return 1
	else:
		return n * factorial(n-1)
```

# 3. Check Prime Number
```python
def isPrime(n):
	if n <= 1:
		return True
	
	x = n // 2
	while x > 1:
		if n % x == 0:
			return False
		x -= 1
	return True
```

# 4. Count Characters
```python
def countChars(s):
	hashmap = {}
	for i in s:
		hashmap[i] = hashmap.get(i, 0) + 1
	return hashmap
```

# 5. Find Largest Element in Array
```python
def largestElement(arr):
	m = float("-inf")
	for i in arr:
		if i > m:
			m = i
	return m
```

# 6. Palindrome Check
```python
def isPalindrome(s):
	return s == s[::-1]
```

# 7. Count Vowels and Consonants
```python
def countVandC(s):
	vowels = "euioa"
	consonants = "qwrtypsdfghjklzxcvbnm"
	v_count = 0
	c_count = 0
	for i in s:
		if i in vowels:
			v_count += 1
		elif i in consonants:
			c_count += 1
	return f"Vowels: {v_count}, Consonants: {c_count}"
```

# 8. Fibonacci Sequence
```python
def fibonacci(n):
	dp = [0, 1]
	if n <= 2:
		return dp[:n]
	
	for i in range(n - 2):
		dp.append(dp[-1] + dp[-2])
	
	return dp
```

# 9. List Comprehension to Square Numbers
```python
def listCompToSquare(arr):
	return [n**2 for n in arr]
```

# 10. Find Common Elements
```python
def findCommon(arr1, arr2):
	return [x for x in arr1 if x in arr2]
```

# 11. Remove Duplicates
```python
def removeDuplicates(arr):
	s = set()
	i = 0
	while i < len(arr):
		value = arr[i]
		if value in s:
			arr.pop(i)
		else:
			s.add(value)
			i += 1
	return arr
```

# 12. Reverse Words in a String
```python
def reverseWords(s):
	words = s.split(" ")
	return " ".join(reversed(words))
```

# 13. Find Second Largest Number
```python
def secondLargest(arr):
	biggest = float("-inf")
	secondBiggest = float("-inf")
	for i in arr:
		if i > secondBiggest:
			if i > biggest:
				secondBiggest = biggest
				biggest = i
			elif i < biggest:
				secondBiggest = i
		
	return secondBiggest
```

# 14. Check Anagrams
```python
def checkAnagrams(s1, s2):
	hashmap1 = {}
	hashmap2 = {}
	for i in s1:
		hashmap1[i] = hashmap1.get(i, 0) + 1
	for i in s2:
		hashmap2[i] = hashmap2.get(i, 0) + 1
	return hashmap1 == hashmap2
```

# 15. Filter Even Numbers
```python
def filterEven(arr):
	return [x for x in arr if x % 2 == 0]
```

# 16. Find Factors of a Number
```python
def findFactors(n):
	result = []
	for i in range(1, (n // 2)+1):
		if n % i == 0:
			result.append(i)
	result.append(n)
	return result
```

# 17. List to Dictionary Conversion
```python
def listsToDict(keys, values):
	result = {}
	for i in range(len(keys)):
		key = keys[i]
		value = values[i]
		result[key] = value
	return result
```

# 18. Check Subset
```python
def isSubset(arr1, arr2):
	for i in arr1:
		if not i in arr2:
			return False
	return True
```

# 19. Sum of Even Numbers
```python
def evenSum(arr):
	return sum([x for x in arr if x % 2==0])
```

# 20. Find Missing Number
```python
def findMissing(arr):
	for i in range(len(arr) - 1):
		if not arr[i] + 1 == arr[i+1]:
			return arr[i] + 1
```

# 21. Check Armstrong Number
```python
def isArmstrong(n):
	result = 0
	for i in str(n):
		result += int(i) ** 3
	return result == n
```

# 22. Count Occurrences of Element
```python
def countElement(arr, n):
	result = 0
	for i in arr:
		if i == n:
			result += 1
	return result
```

# 23. Flatten a List
```python
def flattenList(arr):
	result = []
	for i in arr:
		if type(i) == list:
			result.extend(flattenList(i))
		else:
			result.append(i)
	return result
```

# 24. Dictionary Value Manipulation
```python
def dictManip(d):
	result = {}
	for key in d:
		value = d[key]
		if type(value) in [int, float]:
			value *= 2
		result[key] = value
	return result
```

# 25. Dictionary Filtering
```python
def dictFilter(d, threshold):
	result = {}
	for key in d:
		value = d[key]
		if value > threshold:
			result[key] = value
	return result
```

# 26. Merge Dictionaries
```python
def mergeDict(d1, d2):
	result = {}
	for key in d1:
		value = d1[key]
		if key in d2:
			value = d2[key]
		result[key] = value
	
	for key in d2:
		value = d2[key]
		result[key] = value
	
	return result
```

# 27. List of Dictionaries Filter
```python
def listOfDictFilter(arr, key, value):
	result = []
	for i in arr:
		if i[key] == value:
			result.append(i)
	return result
 ```

# 28. Dictionary Key Sort
```python
def dictKeySort(d):
	result = {}
	for key in sorted(d):
		result[key] = d[key]
	return result
```

# 29. Dictionary Value Sort
```python
def dictValueSort(d):
	result = {}
	for k in sorted(d, key=lambda x: d[x]):
		result[k] = d[k]
	return result
```

# 30. Nested Dictionary Access
```python
def nestedDictAccess(d, key_path):
	result = d.copy()
	for key in key_path:
		if key in result:
			result = result[key]
		else:
			return None
	return result
```

# 31. Maximum of Two Numbers
```python
def find_max(a,b):
    if a>b:
        return a
    else:
        return b
```

# 32. Sum of Array
```python
def summ_array(arr):
    sum = 0
    for i in arr:
        sum += i
    return sum
```

# 33. Reverse a String
```python
def reverse(word):
    reversed_word = ''
    for i in range(-1, -len(word)-1,-1):
        reversed_word += word[i]
    return reversed_word
```

# 34. Check Even or Odd
```python
def check(num):
    if(num%2==0):
        return "Even"
    else:
        return "Odd"
```

# 35. Count Words in a String
```python
def check(sentence):
    return len(sentence.split())
```

# 36. Check Leap Year
```python
def leap(year):
    if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
        return True
    else:
        return False
```

# 37. Capitalize First Letter
```python
def capitaliz(sentence):
    result = []
    for word in sentence.split():
        if word.islower():
            new_word = word[0].upper() + word[1:]
        else:
            new_word = word
        result.append(new_word)
    return ' '.join(result)

```

# 38. Sum of Two Numbers
```python
def sum(a,b):
    return a+b

```

# 39. Check Valid Parentheses
```python
def validParentheses(s):
    stack = []
    mapping = {')': '(', '}': '{', ']': '['}

    for char in s:
        if char in mapping.values():
            stack.append(char)
        elif char in mapping:
            if not stack or stack[-1] != mapping[char]:
                return False
            stack.pop()
    return True
```

# 40. Merge Two Sorted Lists
```python
def mergeTwoSortedLists(arr1, arr2):
    new_list = []
    new_length = len(arr1) + len(arr2)
    pointer1 = 0
    pointer2 = 0
    
    for i in range(new_length):
        if arr1[pointer1] < arr2[pointer2]:
            new_list.append(arr1[pointer1])
            pointer1 = min(len(arr1) - 1, pointer1 + 1)
        else:
            new_list.append(arr2[pointer2])
            pointer2 = min(len(arr2) - 1, pointer2 + 1)
    
    new_list[-1] = max(arr1[-1], arr2[-1])
    
    return new_list
```

# 41. First Non-Repeating Character
```python
def nonRepeat(s):
    for char in s:
        if s.count(char) == 1:
            return s.index(char)
    return -1
```

# 42. Student Grade System
```python
class GradeBook:

    def __init__(self):
        self.students = {}

    def add_student(self,name, grade):
        self.students[name] = grade

    def add_grade(self, name, grade):
        if name in self.students:
            self.students[name].append(grade)
        else:
            print(f"Student {name} not found.")
    def get_average(self,name):
        if name in self.students:
            grades = self.students[name]
            return sum(grades) / len(grades)
        else:
            print(f"Student {name} not found.")
            return None
    def get_highest_scorer(self):
        m = 0
        result = None
        for name in self.students:
            if max(self.students[name])>m:
                m = max(self.students[name])
                result = name
        return result
```

# 43. Bank Account Management
```python
class bankAccount:
    def __init__(self, name, balance):
        self.acc = {name:balance}
        self.name = name
        self.balance = balance

    def deposit(self,amount):

        self.acc[self.name] = amount + self.acc[self.name]
        return f"Deposited,New Balance: {self.acc[self.name]}"

    def withdraw(self,amount):
        if amount < self.acc[self.name]:
            self.acc[self.name] = self.acc[self.name] - amount
            return f"Withdrawal,New balance: {self.acc[self.name]}"
        else:
            return "Insufficient funds"
    def getBalance(self):
        return f"Balance: {self.acc[self.name]}"

    def __str__(self):
        return f"Account of: {self.name}, with balance: {self.balance}"

```

# 44. Intersection of Two Arrays
```python
def intersetion(arr1, arr2):
    result = []
    set1 = set(arr1)
    set2 = set(arr2)
    for x in set1:
        if x in set2:
            result.append(x)
    return result
```

# 45. Check Anagrams
```python
def checkAnagrams(s1, s2):
	hashmap1 = {}
	hashmap2 = {}
	for i in s1:
		hashmap1[i] = hashmap1.get(i, 0) + 1
	for i in s2:
		hashmap2[i] = hashmap2.get(i, 0) + 1
	return hashmap1 == hashmap2
```

# 46.Maximum Subarray(Əzbərlə):
```python
def max_subarray(nums):
    max_current = max_global = nums[0]

    for num in nums[1:]:
        max_current = max(num, max_current + num)
        if max_current > max_global:
            max_global = max_current

    return max_global
```

# 47. Two Sum
```python
def two_sum(nums, target):
    my_map = {}
    for i in range(len(nums)):
         num = nums[i]
         complement = target - num
         if complement in my_map:
             return [my_map[complement], i]
         my_map[num] = i

    return None
```

# 48. Product of Array Except Self
```python
def multipl(array1):
    result = []
    for i in range(len(array1)):
        multiply = 1
        for j in range(len(array1)):
            if j != i:
                multiply *= array1[j]
        result.append(multiply)

    return result
```

# 49. File Handling and Analysis
```python
def fileAnalysis(filename):
    file = open(filename, 'r').readlines()
    hashmap = {}

    for line in file:
        for word in line.split(' '):
            word = word.replace('.', '').replace('\n', '')
            hashmap[word] = hashmap.get(word, 0) + 1

    keys = list(reversed(sorted(hashmap, key=lambda x: hashmap[x])))
    result = []
    for i in range(5):
        result.append((keys[i], hashmap[keys[i]]))
    return result
```

# 50. Shopping Cart Class
```python
class ShoppingCart:
    def __init__(self):
        self.cart = {}
        self.discount = 0

    def add_item(self, name, price, quantity):
        self.cart[name] = {'price': price, 'quantity': quantity}

    def remove_item(self, name, quantity):
        if quantity < self.cart[name]['quantity']:
            self.cart[name]['quantity'] -= quantity
        elif quantity == self.cart[name]['quantity']:
            self.cart.pop(name)
        else:
            return "User doesn't have that much " + name

    def total_price(self):
        result = 0
        for item in self.cart:
            price = (self.cart[item]['price'] - (self.cart[item]['price'] * self.discount)) * self.cart[item]['quantity']
            result += price

        return result

    def apply_discount(self, discount):
        self.discount = discount / 100

    def view_cart(self):
        return self.cart
```

# 51. Temperature Converter Class
```python
class TemperatureConverter:
    def celsius_to_fahrenheit(self, celcius): return celcius * (9 / 5) + 32

    def fahrenheit_to_celsius(self, farenheit): return (farenheit - 32) * (5 / 9)

    def celsius_to_kelvin(self, celcius): return celcius + 273.15

    def kelvin_to_celsius(self, kelvin): return kelvin - 273.15

    def fahrenheit_to_kelvin(self, farenheit): return (farenheit - 32) * (5 / 9) + 273.15

    def kelvin_to_farenheit(self, kelvin): return ((kelvin - 273.15) * (9 / 5)) + 32

```

# 52. Sort Colors
```python
def sortColors(arr):
    hashmap = {}
    result = []
    for i in arr:
        hashmap[i] = hashmap.get(i, 0) + 1

    for i in sorted(hashmap):
        for j in range(hashmap[i]):
            result.append(i)

    return result

```

# 53. Employee Management System
```python
class EmployeeManagementSystem:
    def __init__(self):
        self.employees = {}
        self.departments = {}

    def add_employee(self, id, name, department, salary):
        self.employees[id] = {
            "name": name,
            "department": department,
            "salary": salary
        }
        if not department in self.departments:
            self.departments[department] = {
                'count': 1,
                'avg_salary': salary,
                'max_salary': salary,
                'min_salary': salary,
                'total_salaries': salary
            }
        else:
            self.departments[department]['count'] += 1
            self.departments[department]['avg_salary'] = self.departments[department]['total_salaries'] / \
                                                         self.departments[department]['count']
            self.departments[department]['total_salaries'] += salary
            self.departments[department]['max_salary'] = self.filter_salary_among_department(department, max)
            self.departments[department]['min_salary'] = self.filter_salary_among_department(department, min)

    def filter_salary_among_department(self, department, func):
        salaries = []
        for employee in self.employees:
            if self.employees[employee]['department'] == department:
                salaries.append(self.employees[employee]['salary'])
        return func(salaries)

    def remove_employee(self, id):
        self.employees.pop(id)

    def give_raise(self, id, amount):
        department = self.employees[id]['department']
        self.employees[id]["salary"] += amount
        self.departments[department]['total_salaries'] += amount
        self.departments[department]['avg_salary'] = self.departments[department]['total_salaries'] / \
                                                     self.departments[department]['count']

        self.departments[department]['max_salary'] = self.filter_salary_among_department(department, max)
        self.departments[department]['min_salary'] = self.filter_salary_among_department(department, min)

    def get_department_stats(self, department):
        return self.departments[department]

```

# 54. String Manipulation
```python
def deleteVowels(s):
    vowels = 'euioa'
    result = ''
    for i in s:
        if not i in vowels:
            result += i
    return result

```

# 55. Calendar Event System
```python
class Calendar:
    def __init__(self):
        self.events = {}

    def convert_time_to_int(self, time):
        hours = int(time.split(':')[0])
        minutes = int(time.split(':')[1])
        return hours * 60 + minutes

    def add_event(self, name, date, start, end, description):
        new_start = self.convert_time_to_int(start)
        new_end = self.convert_time_to_int(end)
        if len(self.events) > 1:
            for event in self.events:
                if self.events[event]["date"] == date:
                    if (self.convert_time_to_int(self.events[event]["end"]) > new_start > self.convert_time_to_int(
                            self.events[event]["start"])
                            or self.convert_time_to_int(self.events[event]["end"]) > new_end > self.convert_time_to_int(
                                self.events[event]["start"])):
                        return "Scheduling conflict for " + name + " event!"

        self.events[name] = {
            "date": date,
            "start": start,
            "end": end,
            "description": description
        }

    def get_events_by_date(self, date):
        result = []
        for event in self.events:
            if self.events[event]['date'] == date:
                result.append(self.events[event])
        return result
```

# 56. Data Analysis with Dictionaries
```python
def DAwithDicts(arr):
	cats = {}
	for product in arr:
		if not product["category"] in cats:
			cats[product["category"]] = {
					"total_revenue": product["price"] * product["quantity"],
					"items_sold": product["quantity"],
					"avg_price": product["price"],
					"items": 1,
					"total_price": product["price"]
				}
		else:
			cats[product["category"]]["total_revenue"] += product["price"] * product["quantity"]
			cats[product["category"]]["items_sold"] += product["quantity"]
			cats[product["category"]]["items"] += 1
			cats[product["category"]]["total_price"] += product["price"]
			cats[product["category"]]["avg_price"] = cats[product["category"]]["total_price"] / cats[product["category"]]["items"]
	for cat in cats:
		cats[cat].pop("items")
		cats[cat].pop("total_price")
	return cats
```

# 57. URL Parser Class
```python
class URLParser:
	def _init_(self, url):
		self.scheme = url.split("://")[0]
		self.domain = url.split("://")[1].split("/")[0]
		self.path = url.split(self.domain)[1].split("?")[0]
		self.params = {}
		if "?" in url:
			for param in url.split("?")[1]. split("&"):
				key = param.split("=")[0]
				value = param.split("=")[1]
				self.params[key] = value

	def get_scheme(self): return self.scheme

	def get_domain(self): return self.domain

	def get_path(self): return self.path

	def get_query_params(self): return self.params

	def set_scheme(self, scheme):
		self.scheme = scheme

	def set_domain(self, domain):
		self.domain = domain

	def set_path(self, path):
		self.path = path

	def set_query_param(self, key, value):
		self.params[key] = value

	def get_full_url(self):
		result = self.scheme + "://" + self.domain + self.path
		if len(self.params) == 1:
			param = self.params.keys()[0]
			result += "?" + param + "=" + self.params[param]
		elif len(self.params) > 1:
			result += "?"
			for param in self.params:
				result += param + "=" + self.params[param] + "&"
			result = result[:-1]
		return result
```

# 58. Check if Number is Divisible
```python
def fizzBuzz(n):
	return n % 3 == 0 and n % 5 == 0
```

# 59. Convert Minutes to Hours and Minutes
```python
def convertMinsToHM(minutes):
	return f"{minutes // 60} hours and {minutes % 60} minutes"
```

# 60. Inventory Management System
```python
class InventorySystem:
	def _init_(self):
		self.database = {}

	def add_product(self, id, name, price, amount):
		self.database[id] = {"name": name, "price": price, "amount": amount}

	def record_sale(self, id, amount):
		if amount <= self.database[id]["amount"]:
			self.database[id]["amount"] -= amount

		else:
			return f"Product {self.database[id]['name']} is out of stock!"

	def is_in_stock(self, id, amount):
		return amount <= self.database[id]["amount"]

	def restock(self, id, amount):
		self.database[id]["amount"] += amount

	def get_low_stock_items(self, amount):
		result = []
		for id in self.database:
			if self.database[id]["amount"] < amount:
				result.append(self.database[id])
		return result

	def get_inventory_value(self):
		result = 0
		for id in self.database:
			result += self.database[id]["price"] * self.database[id]["amount"]
		return result
```
