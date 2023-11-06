# lab-6
#1
def get_keys_with_value_true(input_dict):
    result = [key for key, value in in_put.items() if value == True]
    return result

in_put = {
    "a": True,
    "b": False,
    "c": True
}

output = get_keys_with_value_true(in_put)
print(output)  

#2
def get_unique_elements(in_list):
    result = []
    for element in in_list:
        if in_list.count(element) <= 1:
            result.append(element)
    return result

in_list = [1, 2, 3, 1, 2, 4]

output = get_unique_elements(in_list)
print(output) 

#3
def get_date_in_format(date):
    year, month, day = date.split('.')
    
    formatted = f"{day}.{month}.{year}"
    
    return formatted

new_date = "2023.10.23"

output = get_date_in_format(new_date)
print(output)  

#4
def get_elements_with_no_more_than_two_occurrences(input_list):
    result = []
    kolichestvo = {}  

    for element in input_list:
        if element in kolichestvo:
            kolichestvo[element] += 1
        else:
            kolichestvo[element] = 1

    for element, count in kolichestvo.items():
        if count == 2:
            result.append(element)

    return result

input_list = [1, 2, 3, 1, 2, 4]

output = get_elements_with_no_more_than_two_occurrences(input_list)
print(output)  

#5
def get_words_from_string(string):
    words = string.split()
    return words

input_str = "This a string with a several words."

output = get_words_from_string(input_str)
print(output) 

#6
def get_unique_elements_with_count(in_list):
    unique_ones = {}
    for element in in_list:
        if element in unique_ones:
            unique_ones[element] += 1
        else:
            unique_ones[element] = 1
    return unique_ones

in_list = [1, 2, 3, 1, 2, 4, 1, 2]

output = get_unique_elements_with_count(in_list)
print(output)  

#7
def get_prime_numbers(n):
    prime_n = []
    for num in range(2, n+1):
        is_prime = all(num % i != 0 for i in range(2, int(num**0.5) + 1))
        if is_prime:
            prime_n.append(num)
    return prime_n

n = 100

output = get_prime_numbers(n)
print(output) 

#8
def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

def get_prime_numbers_in_list(input_list):
    return [n for n in in_list if is_prime(n)]

in_list = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 27, 36, 48, 54, 67, 71, 73, 75, 83, 89, 99]

output = get_prime_numbers_in_list(in_list)
print(output)  
 
 
#9
from datetime import datetime

def get_difference_between_dates(date1, date2):
    formatted = "%Y.%m.%d"
    delta = abs((datetime.strptime(date2, formatted) - datetime.strptime(date1, formatted)).days)
    return delta


date1 = "2023.10.23"
date2 = "2023.10.24"

output = get_difference_between_dates(date1, date2)
print(output)  


#10
def get_decimal_number_from_binary_string(binary_string):
    decimal_n = int(binary_string, 2)
    return decimal_n

binary_string = "10110011"

output = get_decimal_number_from_binary_string(binary_string)
print(output)  

#11
def is_expression_true(a):
    numbers = a.split(', ')
    return all(int(num)**0.5.is_integer() for num in numbers)

a = "4, 25, 81"

output = is_expression_true(a)
print(output)  

#12
def sort_by_price(fruits):
    sorted_list = sorted(fruits, key=lambda x: x['price'])
    return sorted_list

fruits = [
    {"name": "Apple", "price": 100},
    {"name": "Banana", "price": 50},
    {"name": "Orange", "price": 20}
]

output = sort_by_price(fruits)
print(output)  

#13
def get_words_starting_with_vowel(fruits):
    vowels = "aeiouAEIOU"
    return [word for word in fruits if word[0] in vowels]

fruits = ["apple", "banana", "orange", "bear", "cat"]

output = get_words_starting_with_vowel(fruits)
print(output) 
 
