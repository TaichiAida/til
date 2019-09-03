**friend** function can access the **private** variable.
OK define friend function in class -> define friend function in main file
NG define friend function in class <- define friend function in main file
You cannot define a friend function in main function until a class define a friend function.

**This** is a pointer to the object, so you can write 3 same codes.
```
class Student{
  public:
    Student(int a): var(a){}
    void printInt(){
        cout << var << "\n";
        cout << this->var << "\n";
        cout << (*this).var << "\n";
    }
  prinvate:
    int var;
};
```
