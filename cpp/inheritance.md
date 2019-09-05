# Inheritance
In cpp, **inheritance** is one of the most important consept.  
For example, the children class can be inherited from the parent class.  
In inheritance,  
* children class: calls the parent class, is **Derived class**
* parent class: it is called by children class, is **Base class**.

```
class parent
{
    public:
        parent(){};
        void sayHello(){
            cout << "hello";
        }
};

class children:public parent
{
    public:
        children(){};
};
```
When we use the inheritance, we have to use **colon**.
