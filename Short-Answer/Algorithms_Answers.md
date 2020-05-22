#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) The running time for this problem is O(N). This is because the problem grows linearly--meaning, that as 
we increase n, we increase the operations required for the algorithm in a 1:1 manner. If n=4, the algorithm
requires 4 operations, if n=5 it requires 5 operations, and so on.

b) The running time for this problem is O(n log(n)), because we have two loops that are multiplied together. The parent loop is n and the child loop is log(n), so together they are n * log(n). The reason the child one is log(n) is because n is because the number that cuts it off is doubled everytime (j*=2), 


c) The running time for this problem is O(N). This too is linear, meaning that the amount of operations grows with the size of n. If n = 5, then 5 operations will occur. 

## Exercise II

I think the fastest way to do it would be to take the number of stories n and divide it by half, determine if the egg has or hasn't broken, then divide the range from the midpoint to the lowest floor, floor 1, to the highest floor, floor n. Then repeat until I find the correct floor. 

Example: 
- if n = 20, I would start by dropping an egg from floor 10. If the egg didn't break, I would half the range from the current floor to n (the highest floor), and try with floor 15. If it did break, I would go in the opposite direction, and try floor 5. I wouold continue cutting what's left in half in the appropriate direction until I found the breaking point.
- fun calculations: at 1 billion floor we would find the proper floor in only 29 drops; 1 trillion in 40; and 1 quintillion in only 60!

The reason the amount of eggs required for such large numbers of floors is so low is because we are cutting the remaining floors in half with every drop! This would be log_2(n). The time complexity, then, is O(log(N))
