
### __ FACTORY DESIGN METHOD__
```cpp
#include <iostream>

class Product {
public:
    virtual void use() = 0;
};

class ConcreteProductA : public Product {
public:
    void use() override {
        std::cout << "Using ConcreteProductA." << std::endl;
    }
};

class ConcreteProductB : public Product {
public:
    void use() override {
        std::cout << "Using ConcreteProductB." << std::endl;
    }
};

class Creator {
public:
    virtual Product* factoryMethod() = 0;
};

class ConcreteCreatorA : public Creator {
public:
    Product* factoryMethod() override {
        return new ConcreteProductA();
    }
};

class ConcreteCreatorB : public Creator {
public:
    Product* factoryMethod() override {
        return new ConcreteProductB();
    }
};

int main() {
    // Using ConcreteCreatorA to create ConcreteProductA
    Creator* creatorA = new ConcreteCreatorA();
    Product* productA = creatorA->factoryMethod();
    productA->use();

    // Using ConcreteCreatorB to create ConcreteProductB
    Creator* creatorB = new ConcreteCreatorB();
    Product* productB = creatorB->factoryMethod();
    productB->use();

    // Cleanup (ensure proper memory management)
    delete creatorA;
    delete creatorB;
    delete productA;
    delete productB;

    return 0;
}

In the main code or client code, you use the creator class to create objects
without specifying the concrete classes. The decision of which product class
to instantiate is left to the concrete creator classes.


### __SIGNLETON DESIGN PATTERN__

```cpp
#include <iostream>

class Singleton {
private:
    static Singleton* instance;
    Singleton() {}  // Private constructor to prevent instantiation

public:
    static Singleton* getInstance() {
        if (!instance) {
            instance = new Singleton();
        }
        return instance;
    }

    // Example method
    void someMethod() {
        std::cout << "Singleton method called." << std::endl;
    }
};

// Initialize the static member variable
Singleton* Singleton::instance = nullptr;

int main() {
    // Create an object using the getInstance method
    Singleton* singletonObject = Singleton::getInstance();

    // Now you can call methods on the singletonObject
    singletonObject->someMethod();

    // Note: Since the destructor is not provided in the example, you might want to
    // consider proper cleanup or use smart pointers to manage the memory.

    return 0;
}
Ensures that a class has only one instance and provides a global point to this instance.
```
Creational design patterns in C++ are a set of design patterns that deal with 
object creation mechanisms, trying to create objects in a manner suitable 
to the situation. They abstract the instantiation process, making it more 
flexible and decoupled from the system. There are several creational design 
patterns, and some of the commonly used ones in C++ include:

```
