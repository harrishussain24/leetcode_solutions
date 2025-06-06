# LeetCode Problem 066: Plus One

You are given a large integer represented as an integer array digits, where each digits[i] is the ith digit of the integer. The digits are ordered from most significant to least significant in left-to-right order. The large integer does not contain any leading 0's.

Increment the large integer by one and return the resulting array of digits.
 
Example 1:
Input: digits = [1,2,3]
Output: [1,2,4]
Explanation: The array represents the integer 123.
Incrementing by one gives 123 + 1 = 124.
Thus, the result should be [1,2,4].

Example 2:
Input: digits = [4,3,2,1]
Output: [4,3,2,2]
Explanation: The array represents the integer 4321.
Incrementing by one gives 4321 + 1 = 4322.
Thus, the result should be [4,3,2,2].

Example 3:
Input: digits = [9]
Output: [1,0]
Explanation: The array represents the integer 9.
Incrementing by one gives 9 + 1 = 10.
Thus, the result should be [1,0].
 
Constraints:
1 <= digits.length <= 100
0 <= digits[i] <= 9
digits does not contain any leading 0's.

## ✅ Solutions

Convert List to String:
Loop through each digit in the list and concatenate them into a single string.

Convert String to Integer:
Transform the string representation into an integer using int().

Add One:
Increment the integer by 1.

Convert Back to String:
Use str() to convert the incremented result back into a string.

Split and Convert to Integers:
Loop through the new string and convert each character back into an integer, storing the result in a list.


✅ Pros
Simple and easy to follow.

Works well for most practical input sizes.

Correctly handles carries, e.g. [9,9,9] -> [1,0,0,0].


⚠️ Notes
This solution uses extra space due to the string and list conversions.

For interviews, you may be asked to avoid converting to and from integers/strings and instead handle digit-by-digit logic (especially to practice carry handling).