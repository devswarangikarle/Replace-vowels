# Replace-vowels

You are given a string str of length n consisting of lowercase English letters. Find the vowels in the string and replace each vowel with its following consonant in the alphabetic order. i.e. replace a with b, e to f, i to j and so on.
Input
The first line contains an integer n denoting the length of string str.
The second line contains the string str.

Constraints
1 ≤ n ≤ 3x104
Output
Print the resultant string after changes.

def replace_vowels_with_consonants(n, string):
    vowels = "aeiou"
    result = ""
    
    for char in string:
        if char in vowels:
            if char == 'a':
                result += 'b'
            elif char == 'e':
                result += 'f'
            elif char == 'i':
                result += 'j'
            elif char == 'o':
                result += 'p'
            elif char == 'u':
                result += 'v'
        else:
            result += char 
    return result

n = int(input().strip())
string = input().strip()

print(replace_vowels_with_consonants(n, string))
