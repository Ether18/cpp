### 1. create a function where an integer variable can add,square and cube itself

```cpp
#include <iostream>

using namespace std;

// Function prototype
int modifyNumber(int num, char op);

int main()
{
    // Declare an integer variable
    int number = 5;

    // Perform the addition operation
    int result = modifyNumber(number, 'A');
    cout << "After adding 10, the new value is: " << result << endl;

    // Perform the squaring operation
    result = modifyNumber(number, 'S');
    cout << "After squaring, the new value is: " << result << endl;

    // Perform the cubing operation
    result = modifyNumber(number, 'C');
    cout << "After cubing, the new value is: " << result << endl;

    return 0;
}

// Function definition
int modifyNumber(int num, char op)
{
    // Check which operation to perform
    if (op == 'A')
    {
        // Add 10 to the number
        return num + 10;
    }
    else if (op == 'S')
    {
        // Square the number
        return num * num;
    }
    else if (op == 'C')
    {
        // Cube the number
        return num * num * num;
    }
    else
    {
        // Return the original number if invalid operation
        return num;
    }
}

```

```md
> After adding 10, the new value is: 15
> After squaring, the new value is: 25 
> After cubing, the new value is: 125 
```


### 2. write a program that ask user for three integer value and find the sum and its average and also find the greater number among them using class

```cpp
#include <iostream>
using namespace std;

class Math {
    public:
    void sum(int a, int b,int c) {
        cout<<"Sum:" << (a+b+c) << endl;
    }

    void average(int a,int b,int c) {
        cout<<"Average:" << (a+b+c)/3 << endl;
    }

    void greaterNumber(int a, int b ,int c) {
        cout << "greater number:" << (a>b?(a>c?a:c):(b>c?b:c)) << endl;
    }
};

int main() {
    Math math;
    int a,b,c;
    cout << "Enter three number:";
    cin >> a >> b >> c;
    math.greaterNumber(a,b,c);
    math.sum(a,b,c);
    math.average(a,b,c);
    return 0;
}
```

```md
> Enter three number:78
> 75
> 72
> greater number:78
> Sum:225
> Average:75 
```