# sort-a-given-collection-of-numbers-and-its-length-in-ascending-order-using-Recursive-Insertion-Sort.
from __future__ import annotations
def rec_insertion_sort(collection: list, n: int):
# Checks if the entire collection has been sorted
if len(collection) &lt;= 1 or n &lt;= 1:
return
insert_next(collection, n - 1)
rec_insertion_sort(collection, n - 1)
def insert_next(collection: list, index: int):
# Checks order between adjacent elements
if index &gt;= len(collection) or collection[index - 1] &lt;= collection[index]:
return
# Swaps adjacent elements since they are not in ascending order
collection[index - 1], collection[index] = (
collection[index],
collection[index - 1],
)
insert_next(collection, index + 1)
nums = [4, 3, 5, 1, 2]
print(&quot;\nOriginal list:&quot;)
print(nums)
print(&quot;After applying Recursive Insertion Sort the said list becomes:&quot;)
rec_insertion_sort(nums, len(nums))
print(nums)
nums = [5, 9, 10, 3, -4, 5, 178, 92, 46, -18, 0, 7]
print(&quot;\nOriginal list:&quot;)
print(nums)
print(&quot;After applying Recursive Insertion Sort the said list becomes:&quot;)
rec_insertion_sort(nums, len(nums))
print(nums)
nums = [1.1, 1, 0, -1, -1.1, .1]
print(&quot;\nOriginal list:&quot;)
print(nums)
print(&quot;After applying Recursive Insertion Sort the said list becomes:&quot;)

rec_insertion_sort(nums, len(nums))
print(nums)
