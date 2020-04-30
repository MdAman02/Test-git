# Problem Description

### Problem: [Sorted Adjacent Differences](http://codeforces.com/contest/1339/problem/B)
### Contest: [Codeforces Round #633 (Div. 2)](http://codeforces.com/contest/1339/)
### Statement
[Sorted Adjacent Differences](http://codeforces.com/contest/1339/problem/B)
## Solution
Can be done with a **Dynamic Programming** solution. Taking the *current lake position* and remaining *time* to be spent as two **states** of **DP**. 
Then we can solve the problem *Recursively* or *Iteratively* (hell no!!).
For every state *lake* no. and *time*, the optimal number is determined by:

$ \sum_{i=0}^time $ 

![sum](https://latex.codecogs.com/png.latex?%5Cinline%20%5Cprod)


First, sort the array in Ascending order.
Notice a statement on the problem:
> *It's always possible to find such rearrangement.*

So it has to work for any kind of input. To achieve this, we can take the middle index as *pivot* and take numbers from both side one by one *i.e:* take an index from left, then one from right, next from left and so on.

 Choosing the *pivot*, we have to make sure it doesn't end with taking consequtive index from same side. This way, the adj difference is always greater or equal to previous one.
