# Separate Files for Classes
In general, it is good to define new classes in separate files(Source and Header).  
## Header file
The header file (.h) describes the function and variable.  
For example, if you want to define the **Student** class, you will write the **Student.h** file like below, 
```
// Student.h
#ifndef STUDENT_H
#define STUDENT_H

class Student
{
    public:
        Student();
        void set_name(string s){
            name = s;
        }
        string get_name(){
            return name;    
        }
    protected:
    private:
        string name;
};

#endif
```
As above, it is a little different from when *class* and *main* are written together in one file (.cpp).  
In header file, you have to write some lines,  
* #ifndef (name of class)
* #define (name of class)
* #endif  

First, **#ifndef** is "if not defined" that checks (name of class) has already defined or not.
Then, **#define** can define the class (name of class).
Finally, you have to conclude the file with **#endif**.

## Source file
After you define the class in header file (.h), you can write the main function in the source file (.cpp).  
If you write **Student.h**, you have to **include** it.
```
// Student.cpp
#include <iostream>
#include "Student.h"
using namespace std;

Student::Student(){
    cout << "Hello" << "\n";
}

int main(){
    Student obj;
    return 0;
}

// Output "Hello" by Student().
```
In the code, I wrote "Student::Student(){}".  
You can use for the constructor definition in "(class name)::(member function name)".

