# Two Sum
## https://leetcode.com/problems/two-sum

Given an array of integers, return indices of the two numbers such that they add up to a specific target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

```
Example:

Given nums = [2, 7, 11, 15], target = 9,

Because nums[0] + nums[1] = 2 + 7 = 9,
return [0, 1].
```

## Implementation :

```java
public int[] twoSum(int[] nums, int target) {
        int[] result = {-1, -1};
        if(nums == null || nums.length < 2)
        	return result;
        
        int n = nums.length;
        for(int i = 0; i < n - 1; i++) {
        	for(int j = i + 1; j < n; j++) {
        		if(nums[i] + nums[j] == target) {
        			result[0] = i;
        			result[1] = j;
        		}
        	}
        }
        return result;
}
```
Above implementation have runtime complexity of O(n^2) and space complexity of O(1)

```
Runtime Complexity = O(n^2)
Space Complexity   = O(1)
```
