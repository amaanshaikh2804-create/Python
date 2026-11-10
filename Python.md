# python coding

1.check prime or not

```python
def is_prime(n):
    if n <= 1:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

# Example
num = int(input("Enter a number: "))

if is_prime(num):
    print(f"{num} is a prime number")
else:
    print(f"{num} is not a prime number")
```

2.Check if a number is even or odd.

```python
num = [1,2,3,4,5,6,7,8,9]
for i in num:
    if i % 2 == 0:
        print(i,end=" ")
```

1. Find all prime numbers between 1 to 100.

```python
print("Prime numbers between 1 and 100 are:")

for num in range(2, 101):
    is_prime = True

    for i in range(2, int(num ** 0.5) + 1):
        if num % i == 0:
            is_prime = False
            break

    if is_prime:
        print(num, end=" ")
```

1. Reverse a number.

```python
num = int(input("Enter a number: "))
rev = 0

while num > 0:
    digit = num % 10
    rev = rev * 10 + digit
    num = num // 10

print("Reverse =", rev)
```

1. Count Digits in a Number.                                       

```python
num = int(input("Enter a number: "))
count = 0

while num > 0:
    count += 1
    num //= 10

print("Digits =", count)
```

1. Sum of Digits

```python
num = int(input("Enter a number: "))
sum = 0

while num > 0:
    sum += num % 10
    num //= 10

print("Sum =", sum)
```

1. Find factorial of a number.

```python
num = int(input("Enter a number: "))
fact = 1

for i in range(1, num + 1):
    fact *= i

print("Factorial =", fact)
```

1. Generate Fibonacci series.

```python
n = int(input("Enter terms: "))
a = 0
b = 1

for i in range(n):
    print(a, end=" ")
    c = a + b
    a = b
    b = c
```

1. Check if number is Armstrong.

```python
num = int(input("Enter a number: "))
temp = num
digits = len(str(num))
sum = 0

while temp > 0:
    digit = temp % 10
    sum += digit ** digits
    temp //= 10

if sum == num:
    print("Armstrong")
else:
    print("Not Armstrong")
```

1. Check if number is Palindrome.

```python
num = int(input("Enter a number: "))
temp = num
rev = 0

while temp > 0:
    digit = temp % 10
    rev = rev * 10 + digit
    temp //= 10

if rev == num:
    print("Palindrome")
else:
    print("Not Palindrome")
```

1. Find GCD of two numbers.

```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))

while b != 0:
    a, b = b, a % b

print("GCD =", a)
```

1. Find LCM of two numbers.

```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))

greater = max(a, b)

while True:
    if greater % a == 0 and greater % b == 0:
        print("LCM =", greater)
        break
    greater += 1
```

1. Swap two numbers without temp variable.

```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))

a = a + b
b = a - b
a = a - b

print(a, b)
```

1. Convert decimal to binary.

```python
num = int(input("Enter decimal number: "))
print(bin(num)[2:])
```

1. Convert binary to decimal.

```python
binary = input("Enter binary number: ")
print(int(binary, 2))
```

1. Convert Celsius to Fahrenheit.

```python
c = float(input("Enter Celsius: "))
f = (c * 9 / 5) + 32
print("Fahrenheit =", f)
```

1.  Calculate compound interest.

```python
p = float(input("Principal: "))
r = float(input("Rate: "))
t = float(input("Time: "))

ci = p * ((1 + r / 100) ** t)
print("Amount:", ci)
print("Compound Interest:", ci - p)
```

1. Print multiplication table.

```python
n = int(input("Enter number: "))

for i in range(1, 11):
    print(n, "x", i, "=", n * i)
```

1. Count vowels in a string.

```python
s = input("Enter string: ")
count = 0

for ch in s.lower():
    if ch in "aeiou":
        count += 1

print("Vowels:", count)
```

1. Reverse a string.

```python
s = input("Enter string: ")
print("Reverse:", s[::-1])
```

1. Check if string is palindrome.

```python
s = input("Enter string: ")

if s == s[::-1]:
    print("Palindrome")
else:
    print("Not Palindrome")
```

1.  Count frequency of each character in string.

```python
s = input("Enter string: ")

freq = {}

for ch in s:
    if ch in freq:
        freq[ch] += 1
    else:
        freq[ch] = 1

print(freq)

```

1. Find max and min in an array.

```python
arr = list(map(int, input().split()))

print("Max:", max(arr))
print("Min:", min(arr))
```

1. Find second largest element in array.

```python
arr = [10, 20, 5, 40, 30]

largest = second = float('-inf')

for num in arr:
    if num > largest:
        second = largest
        largest = num
    elif num > second and num != largest:
        second = num

print("Second Largest:", second)
```

1. Remove duplicates from array.

```python
arr = [1, 2, 2, 3, 4, 4, 5]
result = []

for i in arr:
    if i not in result:
        result.append(i)

print(result)  
```

1. Count even & odd elements in array.

```python
arr = [10, 15, 20, 25, 30]

even = odd = 0

for i in arr:
    if i % 2 == 0:
        even += 1
    else:
        odd += 1

print("Even:", even)
print("Odd:", odd)
```

1. Sort array in ascending/descending order.

```python
arr = [5,2,8,1,3]

print("Ascending:",sorted(arr))
print("Descending:",sorted(arr,reverse=True))
```

1. search an element in an array.

```python
arr = [10, 20, 30, 40, 50]
x = int(input("Enter element: "))

if x in arr:
		print("Element found at index:",arr.index(x))
else:
		print("Element not found")
```

1. merge two arrays		
		

```python
arr1 = [1,2,3]
arr2 = [4,5,6]

arr3 = arr1 + arr2

print("Merged array:",arr3)
```

1. add two metrics

```python
A = [[1,2], [3,4]]
B = [[5,6], [7,8]]

C = [[0,0], [0,0]]

for i in range(2):
    for i in range(2):
        c[i][j] = A[i][j] + B[i][j]
        
print("Result:")
for row in C:
    print(row)     
```

1. Transpose a matrix

  

```python
matrix = [[1, 2, 3],
          [4, 5, 6]]

transpose = []

for j in range(len(matrix)):
    row = []
    for i in range(len(matrix)):
        row.append(matrix[i][j])
    transpose.append(row)

print("Transpose:")
for row in transpose:
    print(row)
```

1. sum of each row and column

```python
matrix = [
    [1, 2, 3],
    [4, 5, 6]
]

for j in range (len(matrix[0])):
    total = 0
    for i in range(len(matrix)):
        total += matrix[i][j]
    print("Column", j + 1,"sum =", total)    
```

1. check if matrix is Symmetric

```python
matrix = [
    [1, 2, 3],
    [2, 4, 5],
    [3, 5, 6]
]

symmetric = True

for i in range(len(matrix)):
    for j in range(len(matrix)):
        if matrix[i][j] != matrix[j][i]:
            symmetric = False
            break

if symmetric:
    print("Matrix is symmetric")
else:
    print("Matrix is not symmetric")

```

1. Calculator Using Switch Case

```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
op = input("Enter operator (+, -, *, /): ")

match op:
    case "+":
        print(a + b)
    case "-":
        print(a - b)
    case "*":
        print(a * b)
    case "/":
        print(a / b)
    case _:
        print("Invalid operator")
```

1. Find sum of series: 1+2+3+...+n

```python
n = int(input("Enter n: "))

sum = 0

for i in range(1, n + 1):
    sum = sum + i

print("Sum =", sum)
```

1. Count positive, negative and zero numbers

```python
n = int(input("How many numbers: "))

positive = 0
negative = 0
zero = 0

for i in range(n):
    num = int(input("Enter number: "))

    if num > 0:
        positive += 1
    elif num < 0:
        negative += 1
    else:
        zero += 1

print("Positive =", positive)
print("Negative =", negative)
print("Zero =", zero)
```

1. Print all factors of a number

```python
n = int(input("Enter number: "))

for i in range(1, n + 1):
    if n % i == 0:
        print(i)
```

1. Find the largest prime factor

```python
n = int(input("Enter number: "))

largest = 0

for i in range(2, n + 1):
    if n % i == 0:
        prime = True

        for j in range(2, i):
            if i % j == 0:
                prime = False
                break

        if prime:
            largest = i

print("Largest prime factor =", largest)
```

1. Convert decimal to hexadecimal

```python
n = int(input("Enter decimal number: "))

digits = "0123456789ABCDEF"
result = ""

while n > 0:
    remainder = n % 16
    result = digits[remainder] + result
    n = n // 16

print("Hexadecimal =", result)
```

1. Remove whitespaces from a string

```python
s = input("Enter string: ")

result = ""

for ch in s:
    if ch != " ":
        result = result + ch

print(result)
```

1. Capitalize first letter of every word

```python
s = input("Enter sentence: ")

result = ""
new_word = True

for ch in s:
    if ch == " ":
        result = result + ch
        new_word = True
    else:
        if new_word:
            result = result + ch.upper()
            new_word = False
        else:
            result = result + ch

print(result)
```

1. Find frequency of a word in a sentence

```python
sentence = input("Enter sentence: ")
word = input("Enter word: ")

words = sentence.split()
count = 0

for w in words:
    if w == word:
        count += 1

print("Frequency =", count)
```

1. Print ASCII value of characters

```python
s = input("Enter string: ")

for ch in s:
    print(ch, "=", ord(ch))
```

1. Count words in a sentence

```python
s = input("Enter sentence: ")

words = s.split()

count = 0

for word in words:
    count += 1

print("Number of words =", count)
```

1. Convert string to integer without using built-in

```python
s = input("Enter number: ")

num = 0

for ch in s:
    digit = ord(ch) - ord('0')
    num = num * 10 + digit

print("Integer =", num)
```