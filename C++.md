

- [inline function in c++](https://www.geeksforgeeks.org/inline-functions-cpp/?ref=lbp)
- [size of an empty class](https://www.geeksforgeeks.org/why-is-the-size-of-an-empty-class-not-zero-in-c/?ref=ml_lbp)
- [virtual base class and it use](https://www.geeksforgeeks.org/virtual-base-class-in-c/)
- [smart pointers in c++](https://www.geeksforgeeks.org/auto_ptr-unique_ptr-shared_ptr-weak_ptr-in-cpp/)
- [new and delte keyword in c++](https://www.geeksforgeeks.org/new-and-delete-operators-in-cpp-for-dynamic-memory/)
- [calloc, malloc, realloc in c]()
- [lambda expresssion in c++] (https://www.programiz.com/cpp-programming/lambda-expression)

 ## __understanding it and some ways how to use lambda function__

 ```cpp
#include <iostream>
#include <bits/stdc++.h>

using namespace std;

int main()
{
   // cout<<"Hello World";
    
    vector<int> x{1,2,3,4,5,6,7,8,9,10};
   
   auto l = [&x](int a, int b, int &yy) {
        for(auto &i : x)
        {i=a+b+yy;yy=77777  ;cout<<i<<endl;}
    };
    int c=88;
    l(6,8,c);
    cout<<"hello";
    cout<<c;
  for(auto &i : x)
        {  cout<<i<<endl;
        }
    
    return 0;
}
output::
102
77791
77791
77791
77791
77791
77791
77791
77791
77791
hello77777102
77791
77791
77791
77791
77791
77791
77791
77791
77791

```
EXAXMPLE 2
### __Differences between C and C++__
| C        | C++     |
|----------|---------|
| C was developed by Dennis Ritchie between the year 1969 and 1973 at AT&T Bell Labs. | C++ was developed by Bjarne Stroustrup in 1979. |
|    C does no support polymorphism, encapsulation, and inheritance which means that C does not support object oriented programming.      |    C++ supports polymorphism, encapsulation, and inheritance because it is an object oriented programming language.     |
|   C is a subset of C++.       |   C++ is a superset of C.      |
|    C contains 32 keywords.      |   C++ contains 63 keywords.    |
|   For the development of code, C supports procedural programming.       |    C++ is known as hybrid language because C++ supports both procedural and object oriented programming paradigms.     |
|   Data and functions are separated in C because it is a procedural programming language.       |  Data and functions are encapsulated together in form of an object in C++.       |
|   C does not support information hiding.       |   Data is hidden by the Encapsulation to ensure that data structures and operators are used as intended.      |
|   Built-in data types is supported in C.       |   Built-in & user-defined data types is supported in C++.      |
|    C is a function driven language because C is a procedural programming language.      |  C++ is an object driven language because it is an object oriented programming.       |
|   Function and operator overloading is not supported in C.       |   Function and operator overloading is supported by C++.      |
|   C is a function-driven language.       |  C++ is an object-driven language       |
|   Functions in C are not defined inside structures.       |   Functions can be used inside a structure in C++.      |
|    Namespace features are not present inside the C.      |   Namespace is used by C++, which avoid name collisions.      |
|   Header file used by C is stdio.h.       |  Header file used by C++ is iostream.h.       |
|  Reference variables are not supported by C.        |   Reference variables are supported by C++.      |
|  Virtual and friend functions are not supported by C.        |   Virtual and friend functions are supported by C++.      |
|   C does not support inheritance.       |   C++ supports inheritance.      |
|   Instead of focusing on data, C focuses on method or process.       |  C++ focuses on data instead of focusing on method or procedure.       |
|   C provides malloc() and calloc() functions for dynamic memory allocation, and free() for memory de-allocation.       |   C++ provides new operator for memory allocation and delete operator for memory de-allocation.      |
|   scanf() and printf() functions are used for input/output in C.       |   cin and cout are used for input/output in C++.      |
|   C structures don’t have access modifiers.       |   C ++ structures have access modifiers.      |

### __Similarities between C and C++__
- Both the languages have a similar syntax.
- Code structure of both the languages are same.
- The compilation of both the languages is similar.
- They share the same basic syntax. Nearly all of C’s operators and keywords are also present in C++ and do the same thing.
- C++ has a slightly extended grammar than C, but the basic grammar is the same.
- Basic memory model of both is very close to the hardware.
- Same notions of stack, heap, file-scope and static variables are present in both the languages.

### __Namespace in C++__

Namespaces allow us to group named entities that otherwise would have global scope into narrower scopes, giving 
them namespace scope. This allows organizing the elements of programs into different logical scopes referred to by names.
- mespace is a feature added in C++ and not present in C.
- namespace is a declarative region that provides a scope to the identifiers (names of the types, function, variables etc) inside it.
- Multiple namespace blocks with the same name are allowed. All declarations within those blocks are declared in the named scope.

```cpp
// A program to demonstrate need of namespace
int main()
{
    int value;
    value = 0;
    double value; // Error here
    value = 0.0;
}
Output :

Compiler Error:
'value' has a previous declaration as 'int value'
```
In each scope, a name can only represent one entity. So, there cannot be two variables with the same name
in the same scope. Using namespaces, we can create two variables or member functions having the same name.

```cpp
// Here we can see that more than one variables 
// are being used without reporting any error.
// That is because they are declared in the 
// different namespaces and scopes.
#include <iostream>
using namespace std;
  
// Variable created inside namespace
namespace first
{
    int val = 500;
}
  
// Global variable
int val = 100;
  
int main()
{
    // Local variable
    int val = 200;
  
    // These variables can be accessed from
    // outside the namespace using the scope
    // operator ::
    cout << first::val << '\n'; 
  
    return 0;
}
Output:
500
```


A namespace definition begins with the keyword namespace followed by the namespace name as follows:

namespace namespace_name 
{
   int x, y; // code declarations where 
             // x and y are declared in 
             // namespace_name's scope
}
- Namespace declarations appear only at global scope.
- Namespace declarations can be nested within another namespace.
- Namespace declarations don’t have access specifiers. (Public or private)
- No need to give semicolon after the closing brace of definition of namespace.
- We can split the definition of namespace over several units.
```cpp
// Creating namespaces
#include <iostream>
using namespace std;
namespace ns1
{
    int value()    { return 5; }
}
namespace ns2 
{
    const double x = 100;
    double value() {  return 2*x; }
}
  
int main()
{
    // Access value function within ns1
    cout << ns1::value() << '\n'; 
  
    // Access value function within ns2
    cout << ns2::value() << '\n'; 
  
    // Access variable x directly
    cout << ns2::x << '\n';       
  
    return 0;
}
```
Following is a simple way to create classes in a name space
```cpp
// A C++ program to demonstrate use of class
// in a namespace
#include <iostream>
using namespace std;
  
namespace ns
{
    // A Class in a namespace
    class geek
    {
    public:
        void display()
        {
            cout << "ns::geek::display()\n";
        }
    };
}
  
int main()
{
    // Creating Object of geek Class
    ns::geek obj;
  
    obj.display();
  
    return 0;
}
Output:

ns::geek::display()
```
Class can also be declared inside namespace and defined outside namespace using following syntax
```cpp
// A C++ program to demonstrate use of class
// in a namespace
#include <iostream>
using namespace std;
  
namespace ns
{
    // Only declaring class here
    class geek;
}
  
// Defining class outside
class ns::geek
{
public:
    void display()
    {
        cout << "ns::geek::display()\n";
    }
};
  
int main()
{
    //Creating Object of geek Class
    ns::geek obj;
    obj.display();
    return 0;
}
Output:

ns::geek::display()
```

We can define methods also outside the namespace. Following is an example code.
```cpp
// A C++ code to demonstrate that we can define 
// methods outside namespace.
#include <iostream>
using namespace std;
  
// Creating a namespace
namespace ns
{
    void display();
    class geek
    {
    public:
       void display();
    };
}
  
// Defining methods of namespace
void ns::geek::display()
{
    cout << "ns::geek::display()\n";
}
void ns::display()
{
    cout << "ns::display()\n";
}
  
// Driver code
int main()
{
    ns::geek obj;
    ns::display();
    obj.display();
    return 0;
}
Output:

ns::display()
ns::geek::display()
```
It is also possible to create more than one namespaces in the global space. This can be done in two ways.
- namespaces having different names
```cpp
// A C++ program to show more than one namespaces 
// with different names.
#include <iostream>
using namespace std;
  
// first name space
namespace first
{
   int func() {  return 5; }
}
  
// second name space
namespace second
{
   int func() { return 10; }
}
  
int main()
{
   // member function of namespace
   // accessed using scope resolution operator
   cout << first::func() <<"\n";        
   cout << second::func() <<"\n"; 
   return 0;
}
Output:
5
10
```
- Extending namespaces (Using same name twice)

It is also possible to create two namespace blocks having the same name. The second namespace block is nothing
but actually the continuation of the first namespace. In simpler words, we can say that both the namespaces 
are not different but actually the same, which are being defined in parts.
```cpp
// C++ program to demonstrate namespace exntension
#include <iostream>
using namespace std;
  
// first name space
namespace first 
{ 
   int val1 = 500;  
}
  
// rest part of the first namespace
namespace  first 
{ 
   int val2 = 501;  
}
  
int main()
{
   cout << first::val1 <<"\n";        
   cout << first::val2 <<"\n"; 
   return 0;
}
Output:

500
501
```
Unnamed Namespaces

- They are directly usable in the same program and are used for declaring unique identifiers.
- In unnamed namespaces, name of the namespace in not mentioned in the declaration of namespace.
- The name of the namespace is uniquely generated by the compiler.
- The unnamed namespaces you have created will only be accessible within the file you created it in.
- Unnamed namespaces are the replacement for the static declaration of variables.
```cpp
// C++ program to demonstrate working of unnamed 
// namespaces
#include <iostream>
using namespace std;
  
// unnamed namespace declaration
namespace 
{
   int rel = 300; 
}
  
int main()
{
   cout << rel << "\n"; // prints 300
   return 0;
}
Output:

300
```
