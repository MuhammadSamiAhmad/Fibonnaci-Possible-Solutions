# **Data Structure Assignment #1**
![Fibonacci forms in life](https://tumamocsketchbook.com/wp-content/uploads/2021/05/Screen-Shot-2021-05-26-at-6.04.09-PM-1024x661.png)
### [Fibonacci In Nature](https://www.mathnasium.com/blog/14-interesting-examples-of-the-golden-ratio-in-nature#:~:text=The%20number%20of%20petals%20in,daisy's%2034%2C%20and%20so%20on.)
## *Fibonacci Possible Solutions*
### Submitted by:
#### Muhammad Sami Ahmad Ismail 
#### BN : 15 
#### Section : 2
- 1ST SOLUTION
  (personal diligence i couldn't begin from zero but it solves the problem if i started counting from 1  )
```
#include <iostream>
using namespace std;
int main() {
	int n;
	int y = 0;
	int x = 1;
	int value = 0;
	cout << "Please enter the number location (n)" << endl;
	cin >> n;
	for (int i =0; i <= (n - 2); i++) {
		value = x + y;
		y = x;
		x = value;
	}
	cout << "The fibonacci value of this location is " << value << endl;
}
```
- 2ND SOLUTION (Using Recursion)
```
// Fibonacci Series using Recursion
#include <bits/stdc++.h>
using namespace std;
 
int fib(int n)
{
    if (n <= 1)
        return n;
    return fib(n - 1) + fib(n - 2);
}
 
int main()
{
    int n = 9;
    cout << fib(n);
    getchar();
    return 0;
}
```
- 3RD SOLUTION (Using Binet formula)
```
// C++ Program to find n'th fibonacci Number
#include<iostream>
#include<cmath>
 
int fib(int n) {
  double phi = (1 + sqrt(5)) / 2;
  return round(pow(phi, n) / sqrt(5));
}
 
// Driver Code
int main ()
{
  int n = 9;
  std::cout << fib(n) << std::endl;
  return 0;
}
```
- 4TH SOLUTION (Using Dynamic Programming)
```
// C++ program for Fibonacci Series 
// using Dynamic Programming
#include<bits/stdc++.h>
using namespace std;
 
class GFG{
public:
int fib(int n)
{
    // Declare an array to store
    // Fibonacci numbers.
    // 1 extra to handle
    // case, n = 0
    int f[n + 2];
    int i;
 
    // 0th and 1st number of the
    // series are 0 and 1
    f[0] = 0;
    f[1] = 1;
 
    for(i = 2; i <= n; i++)
    {
       //Add the previous 2 numbers
       // in the series and store it
       f[i] = f[i - 1] + f[i - 2];
    }
    return f[n];
    }
};
 
// Driver code
int main ()
{
    GFG g;
    int n = 9;
    cout << g.fib(n);
    return 0;
}
```
- 5TH SOLUTION (Space optimized method 2)
```

// Fibonacci Series using Space Optimized Method
#include<bits/stdc++.h>
using namespace std;
 
int fib(int n)
{
    int a = 0, b = 1, c, i;
    if( n == 0)
        return a;
    for(i = 2; i <= n; i++)
    {
       c = a + b;
       a = b;
       b = c;
    }
    return b;
}
 
// Driver code
int main()
{
    int n = 9;
     
    cout << fib(n);
    return 0;
}
```
## Fibonacci Solutions Respectively With Same Order As In List
| Time Complexity | Space Complexity |
| ----------- | ----------- |
| O(n) | O(1) | 
| O(n^2) | O(n) |
| O(Log n) | O(1) |
| O(n) | O(n) |
| O(n) | O(1) |
