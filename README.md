# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

Add your answers to this markdown file.

/////
1
(a) The differences in the algorithms running on different devices will cause the actual execution time to be different, even significantly different.

(b) The same asymptotic complexity may hide underlying performance differences, for example, the actual running time of O(n^2) may be different,The running time of algorithm a is 100n^n+10n+10, and the running time of algorithm b is n^2+n. They both belong to O(n^2) time complexity, but in reality, algorithm a is slower than algorithm b.

(c) The specific implementation method and operational differences are not considered，the time complexity of traversing an array and a linked list is O(n), but the memory of an array is allocated continuously, while the memory of a linked list is distributed, so traversing an array is actually faster.

2
by the def of binary search tree time complexity:O(logn),and the time cost will grow logarithmically with number of element n

so we use the growth to estimate 
$log_2 (1000)$ = $10, log_2(10000) = 13.3$
13.3/10 = 1.33
5*1.33 = 6.65 s

3
(a) Different hardware performance, like 1000 elements run on 100tflops hardware, 10000 elements run on 1flops hardware

(b) Different data types，like 1000 elements contain numbers, 10000 elements contain strings

(c) The existence of concurrently running programs occupying system resources and causing performance degradation，When calculating 1000 elements, the system has no other background tasks. When calculating 10000 elements, the system has other high-load tasks in the background.
