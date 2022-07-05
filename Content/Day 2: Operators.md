# [Day 2: Operators](https://www.hackerrank.com)

### Objective
In this challenge, you will work with arithmetic operators. Check out the Tutorial tab for learning materials and an instructional video.

### Task
Given the meal price (base cost of a meal), tip percent (the percentage of the meal price being added as tip), and tax percent (the percentage of the meal price being added as tax) for a meal, find and print the meal’s total cost. Round the result to the nearest integer.

### Example

mealcost = 100
tippercent = 15
taxpercent = 8

A tip of 15% * 100 = 15, and the taxes are 8% * 100 = 8. Print the value 123 and return from the function.


### Function Description
Complete the solve function in the editor below.

solve has the following parameters:

int meal_cost: the cost of food before tip and tax
int tip_percent: the tip percentage
int tax_percent: the tax percentage
Returns The function returns nothing. Print the calculated value, rounded to the nearest integer.

### Note: 
Be sure to use precise values for your calculations, or you may end up with an incorrectly rounded result.

### Input Format
There are 3 lines of numeric input:
The first line has a double, mealcost (the cost of the meal before tax and tip).
The second line has an integer, tippercent (the percentage of mealCost being added as tip).
The third line has an integer, taxpercent (the percentage of mealCost being added as tax).


### Sample Input
```
12.00
20
8
```

### Sample Output
```
15
```

### Explanation


Given:
mealcost = 12, tip_percent = 20, tax_percent = 8

Calculations:
tip = 12 and 12/100 * 20 = 2.4

tax = 8 and 8/100 * 20 = 0.96

total_cost = meal_cost + tip + tax = 12 + 2.4 + 0.96 = 15.36

round(total_cost) = 15

We round total_cost to the nearest integer and print the result, 15.

### Solution – Day 2: Operators Solution


C++

```#include <bits/stdc++.h>

using namespace std;

// Complete the solve function below.
void solve(double meal_cost, int tip_percent, int tax_percent) 
{
    double tip=meal_cost*tip_percent/100;
    double tax=meal_cost*tax_percent/100;
    int totalCost=(int)round(meal_cost+tip+tax);    
    cout<<totalCost;
}

int main()
{
    double meal_cost;
    cin >> meal_cost;
    cin.ignore(numeric_limits<streamsize>::max(), '\n');

    int tip_percent;
    cin >> tip_percent;
    cin.ignore(numeric_limits<streamsize>::max(), '\n');

    int tax_percent;
    cin >> tax_percent;
    
    cin.ignore(numeric_limits<streamsize>::max(), '\n');
    solve(meal_cost, tip_percent, tax_percent);
    
    return 0;
}
```
![photo](https://github.com/Dushyantsingh-ds/30-Days-of-Code-hackerrank/blob/main/Content/Results/Day2.png)




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
