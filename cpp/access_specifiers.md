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
    student myStudent;
    myStudent.name = "TaichiAida";
    cout << myStudent.name << "\n";
    return 0;
}

// Outputs "TaichiAida"
```
Like above code, specifiers must end with a colon (':').
*public* specifier can be accessed from outside the code (like the "main" method).

Second, I will explain the *private* specifier.
```
#include <iostream>
#include <string>
using namespace std;

class student{
    public:
        void setName(string s){
            name = s;
        }
        string getName(){
            return name;
        }
    private:
        string name;
};

int main(){
    student myStudent;
    myStudent.setName("TaichiAida");
    cout << myStudent.getName() << "\n";
    return 0;
}

// Outputs "TaichiAida"
```
According to this code, the *private* specifier can be changed by not outside the code, but inside the code (class).
