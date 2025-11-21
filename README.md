# Core-String-Manipulation-Patterns
The String Manipulation Playbook: Recognizing Patterns for Efficient Problem Solving

## 1. Pointer-Based
 ### a. Single Pointer
 ***When to recognize:*** 
 - You need to process each character exactly once in sequence
 - The solution depends only on the current character or simple running totals
 - No need to compare characters from different positions
 - Can be solved by simple for loop and minimal variables

 ***Common problem patterns:***
 - Character counting - "Count how many times a specific character appears"
 - Running totals - "Calculate sum of digits in a string"
 - Simple validation - "Check if all characters meet a condition"
 - Basic transformations - "Convert case, remove specific characters"

### b. Two Pointers
***When to recognize:*** 
- You need to compare, swap, or check elements from opposite ends or different positions in the string.
- Validating string symmetry or balance

***Common problem patterns:***
- Reverse a string  
- Check if a string is a palindrome
- Valid parentheses (can use two pointers for some variations)
- Visual pattern:
```
"hello" → pointers at 'h' and 'o', move toward center
 ↑   ↑
 l   r
```

### c. Multiple Pointers (K-Pointers)
***When to recognize:*** 
- You need to track multiple positions in a string simultaneously
- Problem involves comparing/processing characters from 3+ different string indices
- You're dealing with multiple conditions or boundaries within one string
- The solution requires partitioning a string into sections

***Common problem patterns:***
1. String Partitioning Problems
- Partition Labels - "Split string into as many parts as possible so each letter appears in at most one part"
- Palindrome Partitioning - "Find all possible ways to partition a string into palindromic substrings"

2. Multiple Boundary Tracking
- Longest Happy Prefix - "Find the longest prefix which is also a suffix"
- Multiple String Segmentation - "Break string into segments based on multiple conditions"

3. Complex Palindrome Problems
- Valid Palindrome III - "Can the string become a palindrome by removing at most K characters?" (may need multiple pointers)
- Longest Palindromic Substring (expanding from multiple centers)

4. String Compression with Multiple Positions

### 2. Sliding Window
***When to recognize:*** 
- You need to find a substring/subarray that meets certain conditions, often involving "longest" or "shortest" with constraints.

***Common problem patterns:***
- Longest substring without repeating characters
- Minimum window substring
- Permutation in string
- Maximum average subarray
- Visual pattern:
```
"abcabcbb" → window expands and contracts based on character repeats
[abc]abcbb → a[bca]bcbb → etc.
```
### 3. Character Counting (Hash Maps)
***When to recognize:***  
You need to track frequency of characters, find anagrams, or check if strings can be rearranged.

***Common problem patterns:***
- Valid anagrams
- Group anagrams
- First unique character in string
- Palindrome permutation
- ***Example thought process:***
-- "If I need to know if two strings have the same characters in different orders, I should count character frequencies."

### 4. String Building
***When to recognize:***  
You need to construct new strings by processing existing ones, often with transformations.

***Common problem patterns:***
- String compression ("aabcccccaaa" → "a2b1c5a3")
- Decode strings ("3[a]2[bc]" → "aaabcbc")
- Zigzag conversion

### 5. Stack-Based Solutions
***When to recognize:*** 
You need to track nested structures, validate sequences, or remove adjacent duplicates.

***Common problem patterns:***
- Valid parentheses
- Remove adjacent duplicates
- Decode nested strings

## Pattern Recognition Framework
When you see a new problem, ask these questions:

1. Does it involve comparing elements from different positions?
 - Yes, from opposite ends → Two Pointers
 - Yes, within a contiguous block → Sliding Window

2. Does it involve counting or frequency?
 - Yes → Hash Map for character counting

3. Does it involve nested or hierarchical structure?
 - Yes → Stack

4. Does it involve building new strings from patterns?
 - Yes → String Building with iteration

5. Am I processing each character in order?
  - Yes → Single Pointer

## Testing your Practice Recognizing Patterns
See if you can identify the pattern before reading the solution:

***Problem 1:*** "Given a string, find the length of the longest substring without repeating characters."

- Your thought process: "I need to find a contiguous block that meets a condition... this sounds like a Sliding Window problem."

***Problem 2:*** "Given two strings s and t, return true if t is an anagram of s."

- Your thought process: "Anagrams have the same characters in different orders... I should count character frequencies with a hash map."

***Problem 3:*** "Given a string containing just parentheses, determine if the input string is valid."

- Your thought process: "Parentheses need to be properly nested and closed... this is a classic Stack problem."



