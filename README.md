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
(a) The amount of input data may be different, for example, n=1000 and n=1
(b) The same asymptotic complexity may hide underlying performance differences, for example, the actual running time of O(n^2) may be different
(c) The specific implementation method and operational differences are not considered

2
by the def of binary search tree time complexity:O(logn),and the time cost will grow logarithmically with number of element n

so we use the growth to estimate 
$log_2 (1000)$ = $10, log_2(10000) = 13.3$
13.3/10 = 1.33
5*1.33 = 6.65 s

3
(a) Different hardware performance
(b) Different data types
(c) The existence of concurrently running programs occupying system resources and causing performance degradation
