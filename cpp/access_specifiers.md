# Access Specifiers
There are some specifiers in the class of C++,
* public
* private
* protected

First, I will write a the example code of *public*.
```
#include <iostream>
#include <string>
using namespace std;

class student{
    public:
        string name;
};

int main(){
    student mystudent;
    mystudent.name = "TaichiAida";
    cout << mystudent.name << "\n";
    return 0;
}

// Outputs "TaichiAida"
```
