# Merge Sorted Array

> You are given two integer arrays nums1 and nums2, sorted in non-decreasing order, and two integers m and n, representing the number of elements in nums1 and nums2 respectively.
 - Merge nums1 and nums2 into a single array sorted in non-decreasing order.
 - The final sorted array should not be returned by the function, but instead be stored inside the array nums1. To accommodate this, nums1 has a length of m + n, where the first m elements denote the elements that should be merged, and the last n elements are set to 0 and should be ignored. nums2 has a length of n.

 ```python
   class Solution(object):
    def merge(self, nums1, m, nums2, n):
        """
        :type nums1: List[int]
        :type m: int
        :type nums2: List[int]
        :type n: int
        :rtype: None Do not return anything, modify nums1 in-place instead.
        """
        i = len(nums1)-1
        while len(nums1) > m:
            if nums1[i] == 0:
                nums1.pop(i)
                i -= 1
        nums1.extend(nums2)
        nums1.sort()
```
