# [Day 4: Class vs. Instance](https://www.hackerrank.com)

### Objective
In this challenge, we’re going to learn about the difference between a class and an instance; because this is an Object Oriented concept, it’s only enabled in certain languages. 

### Task
Write a Person class with an instance variable, age, and a constructor that takes an integer, initialAge, as a parameter. The constructor must assign initialAge to age after confirming the argument passed as initialAge is not negative; if a negative argument is passed as initialAge, the constructor should set age to  0and print Age is not valid, setting age to 0.. In addition, you must write the following instance methods:

yearPasses() should increase the age instance variable by 1. <br>
amIOld() should perform the following conditional actions: <br>
If age < 13, print You are young.. <br>
If age => 13 and age < 18, print You are a teenager.. <br>
Otherwise, print You are old.. <br>
To help you learn by example and complete this challenge, much of the code is provided for you, but you’ll be writing everything in the future. The code that creates each instance of your Person class is in the main method. Don’t worry if you don’t understand it all quite yet!

### Note: Do not remove or alter the stub code in the editor.

### Input Format
Input is handled for you by the stub code in the editor. <br>


The first line contains an integer, T (the number of test cases), and the T subsequent lines each contain an integer denoting the age of a Person instance. <br>

Constraints <br>
1 <= T <= 4 <br>
-5 <= age <= 30 <br>

### Output Format
Complete the method definitions provided in the editor so they meet the specifications outlined above; the code to test your work is already in the editor. If your methods are implemented correctly, each test case will print 2 or 3 lines (depending on whether or not a valid initialAge was passed to the constructor).

### Sample Input

4 <br>
-1 <br>
10 <br>
16 <br>
18 <br>

### Sample Output

Age is not valid, setting age to 0. <br>
You are young. <br>
You are young. <br>

You are young. <br>
You are a teenager. <br>
 
You are a teenager. <br>
You are old. <br>

You are old. <br>
You are old. <br>

### Explanation


Test Case 0: initialAge = -1 <br>
Because initialAge < 0, our code must set age to 0 and print the “Age is not valid…” message followed by the young message. Three years pass and age = 3, so we print the young message again.
<br>
Test Case 1: initialAge = 10 <br>
Because initialAge < 13, our code should print that the person is young. Three years pass and age = 13, so we print that the person is now a teenager.

Test Case 2: initialAge = 16 <br>
Because 13 <= initialAge < 18, our code should print that the person is a teenager. Three years pass and age = 19, so we print that the person is old.
<br>

Test Case 3: initialAge = 18 <br>
Because initialAge => 18, our code should print that the person is old. Three years pass and the person is still old at age = 21, so we print the old message again.
<br>

### Solution – Day 4: Class vs. Instance Solution

C++

```
using namespace std;
#include <iostream>

class Person{
    public:
        int age;
        Person(int initialAge);
        void amIOld();
        void yearPasses();
    };

    Person::Person(int initialAge){
        // Add some more code to run some checks on initialAge
    if(initialAge<0){
    age = 0;
    cout<<"Age is not valid, setting age to 0.\n";
    }else{
        age = initialAge;
    }
    }

    void Person::amIOld(){
        if(age<13){
            cout<<"You are young.\n";
        }else if(age>=13 && age <18){
            cout<<"You are a teenager.\n";
        }else{
            cout<<"You are old.\n";
        }
    }

    void Person::yearPasses(){
        age++;
        // Increment the age of the person in here
    }

int main(){
    int t;
	int age;
    cin >> t;
    for(int i=0; i < t; i++) {
    	cin >> age;
        Person p(age);
        p.amIOld();
        for(int j=0; j < 3; j++) {
        	p.yearPasses(); 
        }
        p.amIOld();
      
		cout << '\n';
    }

    return 0;
}
```
![photo](https://github.com/Dushyantsingh-ds/30-Days-of-Code-hackerrank/blob/main/Content/Results/Day4.png)




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
