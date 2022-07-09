# [Day 6: Let's Review.](https://www.hackerrank.com)

### Objective
Today we will expand our knowledge of strings, combining it with what we have already learned about loops.

### Task
Given a string, S, of length N that is indexed from 0 to N – 1, print its even-indexed and odd-indexed characters as 2 space-separated strings on a single line (see the Sample below for more detail).

## Note: 0 is considered to be an even index.

### Example
 <br>
s = adbecf <br>

 <br>
Print abc def  <br>

### Input Format
The first line contains an integer, T (the number of test cases).  <br>
Each line i of the T subsequent lines contain a string, S.  <br>

### Constraints
For each String Sj (where 0 <= j <= T – 1), print Sj‘s even-indexed characters, followed by a space, followed by Sj‘s odd-indexed characters.  <br>

### Sample Input

``` 
2
Hacker
Rank  
```

### Sample Output

```
Hce akr 
Rn ak  
```
### Explanation

Test Case 0: S = “Hacker”  <br>
S[0] = “H”  <br>
S[1] = “a”  <br>
S[2] = “c”  <br>
S[3] = “k”  <br>
S[4] = “e”  <br>
S[5] = “r”  <br>
The even indices are 0, 2, and 4, and the odd indices are 1, 3, and 5. We then print a single line of 2 space-separated strings; the first string contains the ordered characters from S‘s even indices (Hce), and the second string contains the ordered characters from S‘s odd indices (akr).  <br>

Test Case 1: S = “Rank”  <br>
S[0] = “R”  <br>
S[1] = “a”  <br>
S[2] = “n”  <br>
S[3] = “k”  <br>
The even indices are 0, 2 and 4, and the odd indices are 1, 3 and 5. We then print a single line of 2 space-separated strings; the first string contains the ordered characters from S‘s even indices (Rn), and the second string contains the ordered characters from S‘s odd indices (ak).  <br>


### Solution – Day 6: Let’s Review

C++

```
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */   
  
    int x;
    cin >> x;
    for(int i = 0; i < x; i++){
        string s, s1, s2;
        cin >> s;
        for(int j=0; j < s.size(); j++){
            if(j%2==0){
                s1 += s[j];
            }else{
                s2+= s[j];
            }
        }
        cout << s1 << " " << s2 << endl;
    }
    return 0;
}

```

![photo](https://github.com/Dushyantsingh-ds/30-Days-of-Code-hackerrank/blob/main/Content/Results/Day6.png)




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
