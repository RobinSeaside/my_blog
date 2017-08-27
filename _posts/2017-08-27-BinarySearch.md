---
layout: post
title:  "On binary search"
date:   2017-08-27 22:55:00 +0800
tags: ['algorithm', 'search']
author: "LIU Wang-Sheng"
---

# Introduction
Binary Search (BS) a.k.a. half-interval search, is a search algorithm that finds the position of a target value within a **sorted** array[^1]. Specifically, assume the array has been sorted in ascending order, first the algorithm compares the target value to the middle element of the array; if equal, the search ends with the position of the target value is the position of the middle element, otherwise, the array is divided into left and right parts by taking the middle element as the boundary, and search in the left (right) part if the target value is smaller (larger) than the middle element; the search continues until the target value is found in the array (successful) or the array to be searched becomes empty (unsuccessful).

BS is widely used due to its low level of computational complexity. BS requires O(log(n)) comparisons in the worst case. And the worst-case space complexity is O(1). Despite its search efficiency, the drawback is that the array must be sorted before searching and therefore operations such as insert and delete elements are difficult to implement.

# Python code block
~~~ python
def binary_search(data_list, tval):    
    low = 0
    high = len(data_list) - 1
    while low <= high:        
        mid = (low + high) // 2    # the indice of the middle element      
        if data_list[mid] == tval:
            return mid        
        elif data_list[mid] > tval:
            high = mid - 1        
        else:          
            low = mid + 1    
     return    # tval is not in the list, return none
~~~

# Notes
BS is efficient and can be applied to different types of problems; for specialized data structures (e.g., Hash table), they can be seached even faster.

[^1]: https://en.wikipedia.org/wiki/Binary_search_algorithm