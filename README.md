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
(a) There may be large performance differences on different devices
(b) It will also have an impact in different operating environments, such as system usage and memory usage.
(c) Asymptotic analysis usually selects the worst and best cases and does not reflect the actual average situation.

2
by the def of binary search tree time complexity:O(logn),and the time cost will grow logarithmically with number of element n

so we use the growth to estimate 
$log_2 (1000)$ = $10, log_2(10000) = 13.3$
13.3/10 = 1.33
5*1.33 = 6.65 s

3
(a) An unbalanced binary search tree may result in actual time close to O(log n)
(b) Memory allocation problem
(c) Branch prediction penalty
