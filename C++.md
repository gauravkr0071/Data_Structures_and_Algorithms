```txt

 Embedded systems are becoming more prevalent in our daily lives, from smart home devices to medical equipment. Designing these systems requires expertise in hardware, software, and systems engineering. One way to simplify the design process is through the use of design patterns, which are proven solutions to common design problems. In this article, we'll explore some common design patterns used in embedded systems and how they can help developers create more efficient, reliable, and scalable systems.
Overview of Design Patterns:

Design patterns are proven solutions to common design problems that have been identified and
 refined over time by software developers. They are reusable templates that can be applied to various software development scenarios to simplify the design process and improve code quality.

Design patterns can be categorized into three main types: creational, structural, and behavioral.

Creational patterns are used to create objects and their relationships in a way that is
both flexible and efficient.

Structural patterns are used to organize objects and classes in a way that makes them
more manageable and adaptable.

Behavioral patterns are used to facilitate communication between objects and classes, making it easier to manage complex interactions between different parts of the system.

Using design patterns in software development has several benefits.

 Firstly, it can improve the overall quality of the code by reducing the

likelihood of common design errors. Secondly, design patterns can help
developers save time and effort by providing well-established solutions that can be reused across different projects.
Finally, using design patterns can make software development more efficient
 and scalable by reducing complexity and making code easier to maintain over time.

Why are they important in embedded systems?
Design patterns are particularly important in embedded systems for several reasons.

Firstly, embedded systems typically have limited resources, such as memory and processing power.
 Design patterns can help developers create efficient and optimized code that utilizes these resources in the most effective way possible.
Secondly, embedded systems often require a high degree of reliability and robustness, particularly in safety-critical applications like medical devices or aerospace systems.
Design patterns can help developers create code that is easier to test, verify, and maintain, which can improve the overall reliability of the system.

Thirdly, embedded systems are often designed to perform specific tasks,
such as controlling a motor or collecting sensor data. Design patterns can help developers create code that is more modular and adaptable, making it easier to modify or extend the system to meet changing requirements or specifications.

Finally, embedded systems are becoming increasingly complex and interconnected,
 particularly in the context of the Internet of Things (IoT). Design patterns can help developers manage this complexity by providing well-established solutions to common design problems,
which can help reduce errors and improve overall system performance.

There are three main types of design patterns:
creational, structural, and behavioral. Here's a brief overview of each:

Creational patterns:

Creational design patterns are used to create objects in a way that is both flexible and efficient.
 They provide ways to create objects without exposing the underlying creation logic,
 allowing the code to remain decoupled from the objects being created. This type of
pattern is particularly useful when creating objects that are complex or require a
lot of resources to instantiate. Some common creational design patterns include the
Singleton pattern, the Factory pattern, the Builder pattern, and the Object Pool pattern.


2. Structural patterns:
 Structural design patterns are used to organize objects and classes in a way
 that makes them more manageable and adaptable. They provide ways to compose
 objects into larger structures while keeping the relationships between objects
flexible and maintainable. This type of pattern is particularly useful when dealing
with complex or large-scale systems. Some common structural design patterns include
 the Adapter pattern, the Decorator pattern, the Facade pattern, and the Bridge pattern.


3. Behavioral patterns:
 Behavioral design patterns are used to facilitate communication between objects and
 classes, making it easier to manage complex interactions between different parts of
 the system. They provide ways to encapsulate algorithms and behaviors in a
 way that can be reused across different parts of the system. This type of pattern
 is particularly useful when dealing with systems that require a lot of interactivity
 or dynamic behavior. Some common behavioral design patterns include the Observer
pattern, the State pattern, the Command pattern, and the Strategy pattern.

Design patterns can be applied to many different areas of software development, including embedded systems. Here are a few real-world examples of how design patterns can be used in embedded systems:
Singleton Pattern:
 The Singleton pattern is used to ensure that only one instance of a class is created and used throughout the entire system. In embedded systems, this pattern can be used to manage access to shared resources, such as hardware peripherals or system timers. For example, a single instance of a timer class could be used to manage all timing operations within the system, ensuring that only one timer is active at any given time.
2. Observer Pattern:
 The Observer pattern is used to notify objects of changes in another object's state. In embedded systems, this pattern can be used to monitor changes in sensor data or system parameters. For example, a temperature sensor could be observed by multiple objects in the system, such as a heating or cooling system, to ensure that the temperature stays within a certain range.
3. Factory Pattern:
 The Factory pattern is used to create objects without exposing the creation logic to the calling code. In embedded systems, this pattern can be used to create instances of hardware drivers or other low-level system components. For example, a factory class could be used to create instances of a UART driver for communicating with a serial device, allowing the calling code to remain decoupled from the details of the driver implementation.
4. Decorator Pattern:
 The Decorator pattern is used to add additional behavior to an object at runtime. In embedded systems, this pattern can be used to add functionality to existing hardware peripherals or system components. For example, a decorator class could be used to add additional error-checking functionality to a UART driver, without modifying the original driver implementation.
5. State Pattern:
 The State pattern is used to encapsulate an object's behavior in response to changes in its state. In embedded systems, this pattern can be used to manage the system's behavior in response to different operating modes or states. For example, a system could have different power-saving modes, each with its own set of operating parameters and behaviors, which could be managed using a state machine implemented with the State pattern.
hashtag#EmbeddedSystems has
```
- [refernce varible in c++ IMP](https://www.geeksforgeeks.org/references-in-cpp/)
- [static_cast , dynamic_cast, reinterpret_cast, const cast](https://stackoverflow.com/questions/332030/when-should-static-cast-dynamic-cast-const-cast-and-reinterpret-cast-be-used)
- [static_cast in c++](https://www.geeksforgeeks.org/static_cast-in-cpp/)
- [constexpr in c++](https://www.geeksforgeeks.org/understanding-constexper-specifier-in-cpp/)
- [inline function in c++](https://www.geeksforgeeks.org/inline-functions-cpp/?ref=lbp)
- [size of an empty class](https://www.geeksforgeeks.org/why-is-the-size-of-an-empty-class-not-zero-in-c/?ref=ml_lbp)
- [virtual base class and it use](https://www.geeksforgeeks.org/virtual-base-class-in-c/)
- [smart pointers in c++](https://www.geeksforgeeks.org/auto_ptr-unique_ptr-shared_ptr-weak_ptr-in-cpp/)
- [new and delte keyword in c++](https://www.geeksforgeeks.org/new-and-delete-operators-in-cpp-for-dynamic-memory/)
- [calloc, malloc, realloc in c]()
- [lambda expresssion in c++] (https://www.programiz.com/cpp-programming/lambda-expression)
- [Generic lambda in c++ 14](https://www.geeksforgeeks.org/generalized-lambda-expressions-c14/)
- [passing function as a pramter in c++ 3 ways](https://www.geeksforgeeks.org/passing-a-function-as-a-parameter-in-cpp/)
- [template in c++](https://www.geeksforgeeks.org/generics-in-c/?ref=lbp)
- [multithreading_playlist](https://www.youtube.com/playlist?list=PLk6CEY9XxSIAeK-EAh3hB4fgNvYkYmghp)
- [what are the components of STL in c++](https://www.geeksforgeeks.org/the-c-standard-template-library-stl/)
- [ddeep copy and shallow copy exmples in video explaination](https://www.youtube.com/watch?v=nCAVr_T4DbM&list=PLLYz8uHU480j37APNXBdPz7YzAi4XlQUF&index=55)
- [deafult assignmnet oprtaor in c++ PRETTY ADVANCED](https://www.geeksforgeeks.org/default-assignment-operator-and-references-in-cpp/)
- [Virtual destructor in C++](https://www.youtube.com/watch?v=JXHJZJXKP64)
- [ipc using shared memory easy exmaple](https://dextutor.com/program-for-ipc-using-shared-memory/)
- [ipc using shared memory hard exmaple](https://biendltb.github.io/tech/inter-process-communication-ipc-in-cpp/)
- 
### __muktithreading exampkle__
```cpp
#include <iostream>
#include <vector>
//#include <chrono>
#include <thread>
using namespace std;

void cal(int x)
{ this_thread::sleep_for(chrono::seconds(2));
    cout<<x<<endl;
    
}

int main()
{ 
  thread t1(cal,5);
  thread t2(cal,6);
  
  t1.join();t2.join();
return 0;
}

```

  ## __example passing function as a parameter__
```cpp
#include <iostream>

#include <iostream>
#include <vector>
using namespace std;

// Function template with a template parameter
template <typename T>
void myFunction(T arg) {
    std::cout << "Value: " << arg << std::endl;
}

// Function taking a function template as a parameter
template <typename FunctionType, typename ArgType>
void wrapperFunction(FunctionType func, ArgType arg) {
    std::cout << "Calling wrapper function..." << std::endl;
    func(arg);
}

int main() {
    // Calling wrapper function with the function template
    wrapperFunction(myFunction<int>, 42);
    wrapperFunction(myFunction<double>, 3.14);

    return 0;
}

    
  ```

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
