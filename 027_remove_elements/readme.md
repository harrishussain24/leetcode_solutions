# LeetCode Problem 027: Remove Element

Given an integer array nums and an integer val, remove all occurrences of val in nums in-place. The order of the elements may be changed. Then return the number of elements in nums which are not equal to val.

Consider the number of elements in nums which are not equal to val be k, to get accepted, you need to do the following things:

Change the array nums such that the first k elements of nums contain the elements which are not equal to val. The remaining elements of nums are not important as well as the size of nums.

Return k.

Custom Judge:
The judge will test your solution with the following code:

int[] nums = [...]; // Input array
int val = ...; // Value to remove
int[] expectedNums = [...]; // The expected answer with correct length.
                            // It is sorted with no values equaling val.

int k = removeElement(nums, val); // Calls your implementation

assert k == expectedNums.length;
sort(nums, 0, k); // Sort the first k elements of nums
for (int i = 0; i < actualLength; i++) {
    assert nums[i] == expectedNums[i];
}

If all assertions pass, then your solution will be accepted.

Example 1:
Input: nums = [3,2,2,3], val = 3
Output: 2, nums = [2,2,_,_]
Explanation: Your function should return k = 2, with the first two elements of nums being 2.
It does not matter what you leave beyond the returned k (hence they are underscores).

Example 2:
Input: nums = [0,1,2,2,3,0,4,2], val = 2
Output: 5, nums = [0,1,4,0,3,_,_,_]
Explanation: Your function should return k = 5, with the first five elements of nums containing 0, 0, 1, 3, and 4.
Note that the five elements can be returned in any order.
It does not matter what you leave beyond the returned k (hence they are underscores).
 

Constraints:

0 <= nums.length <= 100
0 <= nums[i] <= 50
0 <= val <= 100

## ✅ Solutions

Iterate through the list with an index i.

If the current element is not equal to the target val:

Keep it in the array.

Count it by increasing output.

Move to the next index.

If the current element equals val:

Remove it using pop(i) (elements shift left).

Save it in removed list.

Do not increment i, since the next element shifts into the current position.

After the loop, append removed items back to the end of nums (for display purposes).

Return output, the count of valid (non-val) elements.

✅ Pros
Easy to follow logic.

Handles in-place removal of target elements correctly.

Preserves order of valid elements.

⚠️ Notes
Uses extra space (removed list), so it's not fully in-place.

Modifies nums only for visual correctness, not required by most problems.

For interview purposes, prefer solutions that use O(1) extra space.