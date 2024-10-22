#### Reflection
The solution that I have implemented has time complexity of $O(n^2)$ and space complexity of $O(1)$.

I could come up with better solution with less time complexity by using **Hash Table**.

```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        Map<Integer, Integer> map = new HashMap<>();
        for (int i = 0; i < nums.length; i++) {
            int complement = target - nums[i];
            if (map.containsKey(complement)) {
                return new int[] { map.get(complement), i };
            }
            map.put(nums[i], i);
        }
        // Return an empty array if no solution is found
        return new int[] {};
    }
}
```

By using hash table approach, we can get time complexity of $O(n)$ and space complexity of $O(n)$.