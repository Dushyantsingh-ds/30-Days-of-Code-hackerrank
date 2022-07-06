# [Day 3: Intro to Conditional Statements](https://www.hackerrank.com)

### Objective
In this challenge, we learn about conditional statements. Check out the Tutorial tab for learning materials and an instructional video.

### Task
Given an integer,n , perform the following conditional actions:

If n is odd, print Weird <br>
If n is even and in the inclusive range of 2 to 5, print Not Weird <br>
If n is even and in the inclusive range of 6 to 20, print Weird <br>
If n is even and greater than 20, print Not Weird <br>
Complete the stub code provided in your editor to print whether or not n is weird. <br>

### Input Format
A single line containing a positive integer, n.

### Constraints
1 <= n <= 100 <br>
Output Format <br>
Print Weird if the number is weird; otherwise, print Not Weird. <br>

### Example
Sample Input 0 <br>

```
3
```
Sample Output 0
```
Weird
```
Sample Input 1
```
24
```
Sample Output 1
```
Not Weird
```
### Explanation
<br>
Sample Case 0: n = 3 <br>
n is odd and odd numbers are weird, so we print Weird. <br>


Sample Case 1: n = 24 <br>
n > 20 and n is even, so it is not weird. Thus, we print Not Weird. <br>

### Solution – Day 3: Intro to Conditional Statements solution


C++ <br>

```#include <bits/stdc++.h>

using namespace std;

string ltrim(const string &);
string rtrim(const string &);



int main()
{
    string N_temp;
    getline(cin, N_temp);

    int N = stoi(ltrim(rtrim(N_temp)));

  if ((N % 2) != 0) {
        printf("Weird\n");
    } else if (N >= 2 && N <= 5) {
        printf("Not Weird\n");
    } else if (N >= 6 && N <= 20) {
        printf("Weird\n");
    } else {
        printf("Not Weird\n");
    }
    
    return 0;
}

string ltrim(const string &str) {
    string s(str);

    s.erase(
        s.begin(),
        find_if(s.begin(), s.end(), not1(ptr_fun<int, int>(isspace)))
    );

    return s;
}

string rtrim(const string &str) {
    string s(str);

    s.erase(
        find_if(s.rbegin(), s.rend(), not1(ptr_fun<int, int>(isspace))).base(),
        s.end()
    );

    return s;
}

```
![photo](https://github.com/Dushyantsingh-ds/30-Days-of-Code-hackerrank/blob/main/Content/Results/Day3.png)




### Connect with me:

[<img align="left" alt="Dushyant Singh | LinkedIn" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/linkedin.svg" />][linkedin]
[<img align="left" alt="Dushyant Singh | Twitter" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/twitter.svg" />][twitter]
[<img align="left" alt="Dushyant Singh | GitHub" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/medium.svg" />][github]
[<img align="left" alt="Dushyant Singh | Medium" width="22px" src="https://raw.githubusercontent.com/iconic/open-iconic/master/svg/globe.svg" />][medium]
[<img align="left" alt="Dushyant Singh | Instagram" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/instagram.svg" />][instagram]
[<img align="left" alt="Dushyant Singh | Facebook" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/facebook.svg" />][facebook]
[<img align="left" alt="Dushyant Singh | Telegram" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/telegram.svg" />][telegram]

<br />

[medium]: https://dushyantsingh-ds.medium.com/
[linkedin]: https://linkedin.com/in/dushyantsingh-ds/
[instagram]: https://www.instagram.com/dushyantsingh.ds/
[twitter]: https://twitter.com/dushyantsingh_d
[facebook]: https://www.facebook.com/dushyantsingh.india
[github]: https://github.com/Dushyantsingh-ds
[telegram]: https://t.me/dushyantsingh_d
