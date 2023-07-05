# python

## Exercise 1:
Write a Python program to calculate the sum of all the numbers in a given list.

Question:
Write a Python function called `sum_list_numbers` that takes a list of numbers as input and returns the sum of all the numbers in the list.

## Solution 1: Sum of all numbers in a list
```python
def sum_list_numbers(numbers):
    """
    Calculates the sum of all the numbers in a given list.

    Args:
        numbers (list): List of numbers.

    Returns:
        int: The sum of all the numbers in the list.
    """
    sum = 0
    for num in numbers:
        sum += num
    return sum
```
**Explanation:**  The function `sum_list_numbers` takes a list of numbers as input. It initializes a variable `sum` to 0, which will store the sum of the numbers. Then, it iterates over each number in the list using a for loop and adds it to the `sum` variable. Finally, it returns the calculated sum.

## Exercise 2:
Write a Python program to find the maximum number in a given list.

Question:
Write a Python function called `find_max_number` that takes a list of numbers as input and returns the maximum number in the list.

## Solution 2: Maximum number in a list
```python
def find_max_number(numbers):
    """
    Finds the maximum number in a given list.

    Args:
        numbers (list): List of numbers.

    Returns:
        int: The maximum number in the list.
    """
    max_num = numbers[0]
    for num in numbers:
        if num > max_num:
            max_num = num
    return max_num
```
**Explanation:**  The function `find_max_number` takes a list of numbers as input. It initializes a variable `max_num` to the first element of the list. Then, it iterates over each number in the list using a for loop and compares it with the current maximum number. If a number is greater than the current maximum, it updates the `max_num` variable. Finally, it returns the maximum number found.

## Exercise 3:
Write a Python program to check if a given number is prime or not.

Question:
Write a Python function called `is_prime` that takes a number as input and returns True if the number is prime, and False otherwise.

## Solution 3: Check if a number is prime
```python
def is_prime(number):
    """
    Checks if a given number is prime.

    Args:
        number (int): The number to be checked.

    Returns:
        bool: True if the number is prime, False otherwise.
    """
    if number < 2:
        return False
    for i in range(2, int(number**0.5) + 1):
        if number % i == 0:
            return False
    return True
```
**Explanation:**  The function `is_prime` takes a number as input. It first checks if the number is less than 2 because numbers less than 2 are not prime. Then, it iterates from 2 to the square root of the number (inclusive) and checks if the number is divisible by any of these values. If it is divisible, it means the number is not prime, and the function returns False. If no divisors are found, it means the number is prime, and the function returns True.

## Exercise 4:
Write a Python program to reverse a given string.

Question:
Write a Python function called `reverse_string` that takes a string as input and returns the reversed version of the string.

## Solution 4: Reverse a string
```python
def reverse_string(string):
    """
    Reverses a given string.



    Args:
        string (str): The string to be reversed.

    Returns:
        str: The reversed string.
    """
    return string[::-1]
```
**Explanation:**  The function `reverse_string` takes a string as input. It uses slicing with a step of -1 to reverse the string. The reversed string is then returned.

## Exercise 5:
Write a Python program to count the occurrences of each element in a given list.

Question:
Write a Python function called `count_element_occurrences` that takes a list of elements as input and returns a dictionary where the keys are the elements and the values are the counts of their occurrences in the list.

## Solution 5: Count occurrences of elements in a list
```python
def count_element_occurrences(elements):
    """
    Counts the occurrences of each element in a given list.

    Args:
        elements (list): List of elements.

    Returns:
        dict: A dictionary with elements as keys and their occurrences as values.
    """
    occurrences = {}
    for element in elements:
        occurrences[element] = occurrences.get(element, 0) + 1
    return occurrences
```
**Explanation:**  The function `count_element_occurrences` takes a list of elements as input. It initializes an empty dictionary called `occurrences` to store the counts of each element. Then, it iterates over each element in the list using a for loop. For each element, it uses the `get()` method of the dictionary to retrieve its current count. If the element is not yet present in the dictionary, it returns 0. The count is incremented by 1, and the updated count is assigned to the element in the dictionary. Finally, the dictionary with element occurrences is returned.

## Exercise 6:
Write a Python program to remove duplicates from a given list.

Question:
Write a Python function called `remove_duplicates` that takes a list of numbers as input and returns a new list with duplicate elements removed.

## Solution 6: Remove duplicates from a list
```python
def remove_duplicates(numbers):
    """
    Removes duplicates from a given list.

    Args:
        numbers (list): List of numbers.

    Returns:
        list: List with duplicate elements removed.
    """
    unique_numbers = []
    for num in numbers:
        if num not in unique_numbers:
            unique_numbers.append(num)
    return unique_numbers
```
**Explanation:**  The function `remove_duplicates` takes a list of numbers as input. It initializes an empty list called `unique_numbers` to store the numbers without duplicates. Then, it iterates over each number in the input list using a for loop. For each number, it checks if it is already present in the `unique_numbers` list using the `not in` operator. If the number is not in the list, it means it is unique, and it is appended to the `unique_numbers` list. Finally, the list without duplicate elements is returned.

## Exercise 7:
Write a Python program to check if two strings are anagrams of each other.

Question:
Write a Python function called `check_anagram` that takes two strings as input and returns True if the strings are anagrams of each other, and False otherwise.

## Solution 7: Check if two strings are anagrams of each other
```python
def check_anagram(str1, str2):
    """
    Checks if two strings are anagrams of each other.

    Args:
        str1 (str): First string.
        str2 (str): Second string.

    Returns:
        bool: True if the strings are anagrams, False otherwise.
    """
    sorted_str1 = sorted(str1)
    sorted_str2 = sorted(str2)
    return sorted_str1 == sorted_str2
```
**Explanation:**  The function `

check_anagram` takes two strings as input. It first sorts both strings using the `sorted()` function, which rearranges the characters in alphabetical order. The sorted strings are then compared using the `==` operator to check if they are equal. If the sorted strings are equal, it means the original strings are anagrams of each other, and the function returns True. Otherwise, it returns False.

## Exercise 8:
Write a Python program to find the average of numbers in a given list.

Question:
Write a Python function called `find_average` that takes a list of numbers as input and returns the average of the numbers.

## Solution 8: Average of numbers in a list
```python
def find_average(numbers):
    """
    Calculates the average of numbers in a given list.

    Args:
        numbers (list): List of numbers.

    Returns:
        float: The average of the numbers.
    """
    if len(numbers) == 0:
        return 0  # Return 0 if the list is empty
    total = sum(numbers)
    average = total / len(numbers)
    return average
```
**Explanation:** The function `find_average` takes a list of numbers as input. It first checks if the list is empty by comparing its length to 0. If the list is empty, it returns 0 as the average. Otherwise, it calculates the sum of all the numbers in the list using the `sum()` function and assigns it to the variable `total`. Then, it divides the `total` by the length of the list to get the average. The average is returned as a floating-point number.

## Exercise 9:
Write a Python program to check if a string is a palindrome.

Question:
Write a Python function called `is_palindrome` that takes a string as input and returns True if the string is a palindrome, and False otherwise. A palindrome is a word, phrase, number, or other sequence of characters that reads the same forward and backward.

## Solution 9: Check if a string is a palindrome
```python
def is_palindrome(string):
    """
    Checks if a given string is a palindrome.

    Args:
        string (str): The string to be checked.

    Returns:
        bool: True if the string is a palindrome, False otherwise.
    """
    reversed_string = string[::-1]
    return string == reversed_string
```
**Explanation:** The function `is_palindrome` takes a string as input. It uses string slicing with a step of -1 (`[::-1]`) to reverse the string and assigns it to the variable `reversed_string`. Then, it compares the original string with the reversed string using the `==` operator. If the two strings are equal, it means the original string is a palindrome, and the function returns True. Otherwise, it returns False.


## Exercise 10:
Write a Python program to find the factorial of a given number.

Question:
Write a Python function called `factorial` that takes a number as input and returns its factorial. The factorial of a non-negative integer n, denoted by n!, is the product of all positive integers less than or equal to n.

## Solution 10: Factorial of a number
```python
def factorial(n):
    """
    Calculates the factorial of a given number.

    Args:
        n (int): The number for which factorial is to be calculated.

    Returns:
        int: The factorial of the number.
    """
    if n < 0:
        return None  # Factorial is not defined for negative numbers
    elif n == 0 or n == 1:
        return 1
    else:
        result = 1
        for i in range(2, n + 1):
            result *= i
        return result
```
**Explanation:** The function `factorial` takes a number `n` as input. It first checks if the number is negative. If it is negative, the factorial is not defined, so the function returns `None`. If the number is 0 or 1, the factorial is defined as 1, so the function returns 1. For numbers greater than 1, it initializes a variable `result` to 1. It then iterates over a range starting from 2 up to `n + 1` (inclusive) using a for loop. In each iteration, it multiplies the current value of `result` by the current number `i`. After the loop completes, it returns the final value of `result`, which represents the factorial of the given number.

## Exercise 11:
Write a Python program to check if a given year is a leap year.

Question:
Write a Python function called `is_leap_year` that takes a year as input and returns True if the year is a leap year, and False otherwise. A leap year is a year that is exactly divisible by 4, except for years that are divisible by 100. However, years that are divisible by 400 are leap years.

## Solution 11: Check if a year is a leap year
```python
def is_leap_year(year):
    """
    Checks if a given year is a leap year.

    Args:
        year (int): The year to be checked.

    Returns:
        bool: True if the year is a leap year, False otherwise.
    """
    if year % 4 == 0:
        if year % 100 == 0:
            if year % 400 == 0:
                return True
            else:
                return False
        else:
            return True
    else:
        return False
```
**Explanation:** The function `is_leap_year` takes a year as input. It checks if the year is divisible by 4 using the modulo operator `%`. If it is divisible by 4, it checks if it is also divisible by 100. If it is divisible by 100, it further checks if it is divisible by 400. If it is divisible by 400, it returns True because it is a leap year. If it is divisible by 100 but not by 400, it returns False because it is not a leap year. If the year is not divisible by 100, it returns True because it is a leap year. If the year is not divisible by 4, it returns False because it is not a leap year.

## Exercise 12:
Write a Python program to find the longest word in a given sentence.

Question:
Write a Python function called `find_longest_word` that takes a sentence as input and returns the longest

 word in the sentence. Assume that the sentence only contains letters, spaces, and punctuation marks.

## Solution 12: Find the longest word in a sentence
```python
import re

def find_longest_word(sentence):
    """
    Finds the longest word in a given sentence.

    Args:
        sentence (str): The sentence to be processed.

    Returns:
        str: The longest word in the sentence.
    """
    words = re.findall(r'\w+', sentence)
    longest_word = max(words, key=len)
    return longest_word
```
**Explanation:** The function `find_longest_word` takes a sentence as input. It first uses the `re.findall()` function from the `re` module to extract all the words from the sentence. The regular expression pattern `r'\w+'` matches one or more word characters. The resulting list of words is stored in the variable `words`. Then, the `max()` function is used with the `key=len` argument to find the longest word from the list based on their lengths. The longest word is returned as the output of the function.


## Exercise 13:
Write a Python program to find the common elements between two lists.

Question:
Write a Python function called `find_common_elements` that takes two lists as input and returns a new list containing the common elements between the two lists.

## Solution 13: Find common elements between two lists
```python
def find_common_elements(list1, list2):
    """
    Finds the common elements between two lists.

    Args:
        list1 (list): The first list.
        list2 (list): The second list.

    Returns:
        list: A new list containing the common elements.
    """
    common_elements = []
    for element in list1:
        if element in list2:
            common_elements.append(element)
    return common_elements
```
**Explanation:** The function `find_common_elements` takes two lists, `list1` and `list2`, as input. It initializes an empty list called `common_elements` to store the common elements. It then iterates over each element in `list1` using a for loop. For each element, it checks if it is also present in `list2` using the `in` operator. If an element is found in both lists, it is appended to the `common_elements` list. Finally, the `common_elements` list is returned as the output of the function.

## Exercise 14:
Write a Python program to check if a given string is a valid email address.

Question:
Write a Python function called `is_valid_email` that takes a string as input and returns True if the string is a valid email address, and False otherwise. A valid email address should have a proper format, including an email username, the "@" symbol, and a domain name.

## Solution 14: Check if a string is a valid email address
```python
import re

def is_valid_email(email):
    """
    Checks if a given string is a valid email address.

    Args:
        email (str): The string to be checked.

    Returns:
        bool: True if the string is a valid email address, False otherwise.
    """
    pattern = r'^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$'
    if re.match(pattern, email):
        return True
    else:
        return False
```
**Explanation:** The function `is_valid_email` takes a string `email` as input. It uses regular expressions (`re`) to match the email pattern. The regular expression pattern `r'^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$'` represents the following:
- `^[a-zA-Z0-9._%+-]+`: Matches one or more alphanumeric characters, periods, underscores, percent signs, plus signs, or hyphens at the beginning of the string.
- `@`: Matches the "@" symbol.
- `[a-zA-Z0-9.-]+`: Matches one or more alphanumeric characters, periods, or hyphens for the domain name.
- `\.`: Matches the "." symbol.
- `[a-zA-Z]{2,}$`: Matches two or more alphabetic characters for the domain extension at the end of the string.

If the given `email` matches the pattern, the function returns True; otherwise, it returns False.

## Exercise 15:
Write a Python program to sort a list of numbers in ascending order.

Question:
Write a Python function called `sort_numbers` that takes a list of numbers as input and returns a new list with the numbers sorted in ascending order.

## Solution 15: Sort a list of numbers in ascending order
```python
def sort_numbers(numbers):
    """
    Sorts

 a list of numbers in ascending order.

    Args:
        numbers (list): List of numbers.

    Returns:
        list: A new list with the numbers sorted in ascending order.
    """
    sorted_numbers = sorted(numbers)
    return sorted_numbers
```
**Explanation:** The function `sort_numbers` takes a list of numbers, `numbers`, as input. It uses the `sorted()` function to sort the numbers in ascending order. The sorted numbers are stored in a new list called `sorted_numbers`, which is then returned as the output of the function.

## Exercise 16:
Write a Python program to count the frequency of elements in a list.

Question:
Write a Python function called `count_frequency` that takes a list of elements as input and returns a dictionary containing the frequency of each element in the list.

## Solution 16: Count the frequency of elements in a list
```python
def count_frequency(elements):
    """
    Counts the frequency of elements in a list.

    Args:
        elements (list): List of elements.

    Returns:
        dict: A dictionary containing the frequency of each element.
    """
    frequency = {}
    for element in elements:
        if element in frequency:
            frequency[element] += 1
        else:
            frequency[element] = 1
    return frequency
```
**Explanation:** The function `count_frequency` takes a list of elements, `elements`, as input. It initializes an empty dictionary called `frequency` to store the frequency of each element. It then iterates over each element in the list using a for loop. For each element, it checks if it already exists as a key in the `frequency` dictionary. If it exists, it increments its corresponding value by 1. If it does not exist, it adds the element as a key to the `frequency` dictionary with an initial value of 1. Finally, the `frequency` dictionary is returned as the output of the function.

## Exercise 17:
Write a Python program to reverse a string.

Question:
Write a Python function called `reverse_string` that takes a string as input and returns a new string with the characters reversed.

## Solution 17: Reverse a string
```python
def reverse_string(string):
    """
    Reverses a given string.

    Args:
        string (str): The string to be reversed.

    Returns:
        str: A new string with the characters reversed.
    """
    reversed_string = string[::-1]
    return reversed_string
```
**Explanation:** The function `reverse_string` takes a string, `string`, as input. It uses string slicing with a step of -1 (`[::-1]`) to reverse the string. The reversed string is stored in a new variable called `reversed_string`, which is then returned as the output of the function.

## Exercise 18:
Write a Python program to remove duplicates from a list.

Question:
Write a Python function called `remove_duplicates` that takes a list as input and returns a new list with duplicates removed, preserving the original order of elements.

## Solution 18: Remove duplicates from a list
```python
def remove_duplicates(lst):
    """
    Removes duplicates from a given list.

    Args:
        lst (list): The list to be processed.

    Returns:
        list: A new list with duplicates removed.
    """
    unique_lst = []
    for item in lst:
        if item not in unique_lst:
            unique_lst.append(item)
    return unique_lst
```
**Explanation:** The function `remove_duplicates` takes a list, `lst`, as input. It initializes an empty list called `unique_lst` to store the unique elements. It then iterates over each item in the list using a for loop. For each item, it checks if it is not already present

 in the `unique_lst` using the `not in` operator. If the item is not in the list, it appends it to the `unique_lst`. This ensures that only the first occurrence of each item is added to the `unique_lst`, effectively removing duplicates. Finally, the `unique_lst` is returned as the output of the function.

## Exercise 19:
Write a Python program to find the second largest number in a list.

Question:
Write a Python function called `find_second_largest` that takes a list of numbers as input and returns the second largest number in the list.

## Solution 19: Find the second largest number in a list
```python
def find_second_largest(numbers):
    """
    Finds the second largest number in a list of numbers.

    Args:
        numbers (list): List of numbers.

    Returns:
        float: The second largest number in the list.
    """
    unique_numbers = set(numbers)
    if len(unique_numbers) < 2:
        return None
    else:
        unique_numbers.remove(max(unique_numbers))
        return max(unique_numbers)
```
**Explanation:** The function `find_second_largest` takes a list of numbers, `numbers`, as input. It first creates a set called `unique_numbers` from the list to remove any duplicate numbers. Then, it checks if the length of the `unique_numbers` set is less than 2. If there are less than 2 unique numbers in the list, it means there is no second largest number, so the function returns `None`. Otherwise, it removes the maximum number from the `unique_numbers` set using the `remove()` method. Finally, it returns the maximum number from the modified `unique_numbers` set, which represents the second largest number in the original list.

## Exercise 20:
Write a Python program to calculate the sum of all the elements in a list.

Question:
Write a Python function called `calculate_sum` that takes a list of numbers as input and returns the sum of all the elements in the list.

## Solution 20: Calculate the sum of elements in a list
```python
def calculate_sum(numbers):
    """
    Calculates the sum of all the elements in a list of numbers.

    Args:
        numbers (list): List of numbers.

    Returns:
        float: The sum of all the elements in the list.
    """
    total = sum(numbers)
    return total
```
**Explanation:** The function `calculate_sum` takes a list of numbers, `numbers`, as input. It uses the built-in `sum()` function to calculate the sum of all the numbers in the list. The sum is stored in a variable called `total`, which is then returned as the output of the function.

