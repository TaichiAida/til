# Constant in class
C++ has an expression, **constants**.
It cannot be changed while the program is running.  
All constant variables **must** be initialized at the time of their definition.
```
const int x = 123;
```
We can define the class as **const class** in main function.
```
// Student.h
...
class Student{
    public:
        Student();
        void myname() const;
};

// Student.cpp

#include "Student.h"
#include <iostream>
using namespace std;

void Student::myname() const{
    cout << "Hi" << "\n";
}

int main(){
    const Student obj;
    obj.myname();
}

// Output "Hi"
```

In "Student.h", I set the const function as **void myname() const;**.  
As this code, we have to define the **const** at the **last**.



