# Sorting Algorithms

## Arrays
- Collection of values or variables arranged contiguously (New values cannot be added in the array as the structure is fixed.)
- The values are identified and accessed by its index, which typically starts from 0

### Types of Arrays
- One dimensional
- Multi-dimensional

## Search Algorithms
A search algorithm is designed to solve a search problem.

### Linear Search
- Works by searching each of the element of the array one by one until the target value is found or the array ends
- Time complexity of O(n) (linear)

### Binary Search
- Only works on sorted arrays (data must be sorted in the array)
- It works by repeatedly dividing the array in half, and comapring the target value to the middle element, narrowing down the search range.
- Time complexity of O(log n) (logarithmic)

## Sorting Algorithms
- Sorting algorithms are used to arrange data in a specific order (numerical, alphabetical, or custom) to make data management, retrieval, and analysis efficient.

### Bubble Sort
- Repeatedly steps through the list, compares each pair of adjacent elements, and swaps them if they are in the wrong order .
- Time complexity of O(n²)

Steps:
1. Compare the first two elements.
2. Swap if the first is larger than the second.
3. Move to the next pair and repeat until the end of the array.
4. Repeat the entire process for the remaining unsorted portion.

Example:

<img width="1354" height="629" alt="image" src="https://github.com/user-attachments/assets/3661f01d-7361-42a2-ad72-e120f529a0dd" />

<img width="690" height="313" alt="image" src="https://github.com/user-attachments/assets/4ec8ff97-657d-471a-bc80-11772ef471e6" />

<img width="690" height="313" alt="image" src="https://github.com/user-attachments/assets/52b13a75-f82a-4814-bff8-cb773e8e5241" />

### Selection Sort
- Repeatedly selects the smallest (or largest) element from the unsorted portion of the array and swaps it with the first unsorted element.
- Time complexity of O(n²)

Steps:
1. Find the smallest element in the unsorted portion.
2. Swap it with the first unsorted element.
3. Move the boundary of the sorted portion one element to the right.
4. Repeat the process until the entire array is sorted.

Example:

<img width="690" height="313" alt="image" src="https://github.com/user-attachments/assets/88b25d08-3a3f-48df-8f7f-5df9196f36c5" />

<img width="690" height="313" alt="Screen Shot 05-14-26 at 11 04 AM 001" src="https://github.com/user-attachments/assets/f982fbba-19bc-4676-979d-97fedc29fa9d" />

<img width="690" height="313" alt="image" src="https://github.com/user-attachments/assets/b48e514c-1a03-49ab-aa94-444c2eb3d3c1" />

<img width="690" height="313" alt="image" src="https://github.com/user-attachments/assets/e038c87f-0b47-449a-8a02-423d28064464" />

<img width="690" height="313" alt="image" src="https://github.com/user-attachments/assets/bb0166b7-0854-490d-a7eb-793d3a6c7050" />

<img width="690" height="313" alt="image" src="https://github.com/user-attachments/assets/cfcb6e5a-8593-4323-bed8-dc1fa6c19e1a" />

### Insertion Sort
- Builds the sorted array one element at a time by repeatedly taking the next unsorted element and inserting it into its correct position in the already sorted portion.
- Time complexity of O(n²) , Ω (n)

Steps:
1. Start with the second element as a "key."
2. Compare the key to the elements before it.
3. Shift elements to the right to make space, and insert the key into the correct position.
4. Repeat for all remaining elements.

Example:

<img width="690" height="363" alt="image" src="https://github.com/user-attachments/assets/70d5f58c-88d3-4337-bd02-8096a551bdb3" />

### Merge Sort
A divide and conquer algorithm that recursively divides the array in half until each half contains one element, then merges the halves back together in sorted order.


Steps:
1. Divide the array into two halves.
2. Recursively sort each half. The value is said to be sorted when it is left only a single value
3. Merge the two sorted halves together by comparing the smallest elements.

Example:

<img width="690" height="363" alt="image" src="https://github.com/user-attachments/assets/7b2336ea-5047-4adf-8fc6-a3b2ffa1ab11" />

<img width="690" height="363" alt="image" src="https://github.com/user-attachments/assets/b2cbbafe-27ba-4b86-adbe-ff66fd34ca7c" />

<img width="690" height="363" alt="image" src="https://github.com/user-attachments/assets/4a440828-d669-4fb5-9737-39bf605444e6" />

<img width="690" height="363" alt="image" src="https://github.com/user-attachments/assets/8febc383-9b8a-41fe-bf5e-8fee5924528a" />

## Quick Sort
- A divide and conquer algorithm that selects a "pivot" element and partitions the array into elements smaller than the pivot and elements larger than the pivot.
- Time Complexity: O(n log n), But O(n²) for poor choice of pivot. If the pivot is chosen on as the middle of the value, time complexity will be O(n log n). However, if the pivot is chosen on as either the extreme value (max or min), time complexity will be O(n²)

Steps:
1. Pick a pivot (usually the first, last, or middle element).
2. Partition the array such that all elements less than the pivot are on the left, and all elements greater are on the right.
3. Recursively apply quick sort to the left and right sub arrays.

Example: Quick sort with Pivot on the last element

<img width="1857" height="693" alt="image" src="https://github.com/user-attachments/assets/e02e6b20-1e63-43f7-9de3-075622f7ac8b" />

<img width="1857" height="693" alt="image" src="https://github.com/user-attachments/assets/d9111499-e529-4303-a11a-40932cc1a5d0" />

<img width="1857" height="684" alt="image" src="https://github.com/user-attachments/assets/08d26797-8c3b-4bcc-a224-7042b0a55dc2" />

<img width="1857" height="684" alt="image" src="https://github.com/user-attachments/assets/c953fda9-2140-417a-bf7b-603eba82b2eb" />

<img width="1857" height="684" alt="image" src="https://github.com/user-attachments/assets/8b2d7cb9-83fd-48cf-83c7-bf86a7971904" />
