# Round down
Yesterday, I attend the [Atcoder](https://atcoder.jp/?lang=en) competition.
I answered the problems of A, B, and C.
However, in problem [D-ModSum](https://atcoder.jp/contests/abc139/tasks/abc139_d?lang=en),  
I could not get the AC.  
This problem can be solved by using the sum of the 1 to N-1.  
I wrote the code like below,  
```
n = int(input())
print(int((n-1)*n/2))
```
This code seems to be good, but it cannot consider calculation error.  
Hense, I had to write,  
```
n = int(input())
print((n-1)*n//2)
```
As above, **//** can round down the result of division.
