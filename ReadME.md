# Problem Description

### Problem: [Sorted Adjacent Differences](http://codeforces.com/contest/1339/problem/B)
### Contest: [Codeforces Round #633 (Div. 2)](http://codeforces.com/contest/1339/)
### Statement
[Sorted Adjacent Differences](http://codeforces.com/contest/1339/problem/B)
## Solution
Can be done with a **Dynamic Programming** solution. Taking the *current lake position* and remaining *time* to be spent as two **states** of **DP**. 
Then we can solve the problem *Recursively* or *Iteratively* (hell no!!).
For every state; *ith* lake and *time*, the optimal number is determined by the recursive formula:

![formula](http://www.sciweavers.org/tex2img.php?eq=f_%7Bi%2Ct%7D%5C%20%3D%5C%20%5Cmax_%7Bk%3D1%7D%5E%7Bt%7D%5C%20%28%5C%20g_%7Bi%2Ck%7D%5C%20%2B%5C%20f_%7Bi%2Ct-k-travel%5C_time%7D%5C%20%29&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0)

![img](http://www.sciweavers.org/tex2img.php?eq=f_%7Bi%2Ct%7D%5C%20%3D%5C%20%5Cmax_%7Bk%3D1%7D%5E%7Bt%7D%5C%20%28%5C%20g_%7Bi%2Ck%7D%5C%20%2B%5C%20f_%7Bi%2Ct-k-travel%5C_time%7D%5C%20%29&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0)


![imge](http://www.sciweavers.org/tex2img.php?eq=%20%5Csqrt%7Bab%7D%20&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0)


Where,
* *f<sub>i,t</sub>* denotes - *maximum number of fish caught arriving ith lake with t time remaining*
* *g<sub>i,k</sub>* denotes - *number of fish to be caught at ith lake given k time*

First, sort the array in Ascending order.
Notice a statement on the problem:
> *It's always possible to find such rearrangement.*

So it has to work for any kind of input. To achieve this, we can take the middle index as *pivot* and take numbers from both side one by one *i.e:* take an index from left, then one from right, next from left and so on.

 Choosing the *pivot*, we have to make sure it doesn't end with taking consequtive index from same side. This way, the adj difference is always greater or equal to previous one.
