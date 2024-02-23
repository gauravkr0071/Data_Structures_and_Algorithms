- For objects that are declared as const , you can only call constant member functions.
 The compiler ensures that the constant object is never modified. You can call
either constant or non-constant member functions for a non-constant object.
- you cannot declare a non member function with const keyword, even if you are not
  changing any varaible in that function, simply c++ dont allow const keyword with
  non member function (that is function defined in global scope or which is not a
  part of any class)
  
  - https://www.geeksforgeeks.org/const-member-functions-c/
  - When a function is declared as const, it can be called on any type of object, const object as well as non-const objects.
  - Whenever an object is declared as const, it needs to be initialized at the time of declaration. however, the object initialization while declaring is possible only with the help of constructors.
- A function becomes const when the const keyword is used in the function’s declaration. The idea of const functions is not to allow them to modify the object on which they are called.
- It is recommended practice to make as many functions const as possible so that accidental changes to objects are avoided.

  __CONST KEYWORD__

  ```cpp

  /******************************************************************************

                            Online C Compiler.
                Code, Compile, Run and Debug C program online.
Write your code in this editor and press "Run" button to compile and execute it.

*******************************************************************************/

#include <stdio.h>
int reverse(int x)
{
    int temp = 0x12345678;
    int ans =0;
    int count=3;
    for(int i=0;i<4;i++)
    {
        int byte = temp& (0xFF);
        temp =temp>>8;
        ans |= byte<<(count *8);    
        count--;
        
    }
    
    
    printf("%x",ans);
}

int alternate_swap(int x)
{
    // 1010 1101 0101 0110
    //  A    D    5    6
    // 0101 1110 1010 1001
    //  5    e    a    9
    
    int a = 0xAAAA & x;
     a= a>>1;
    
    int b= 0x5555 & x;
    b=b<<1;
    
    printf("%X",a|b);
    
}
//#include <stdio.h>

// Declare a const volatile variable
const int sharedVariable = 10;

// Function to modify the shared variable
void modifySharedVariable() {
    // Attempt to modify the shared variable
    // Even though it's declared as const, this code will compile
    // However, it violates the const qualifier and may lead to undefined behavior
 printf("heklo");
   *((int*)&sharedVariable) = 20;
}

int main() {
    // Display the initial value of the shared variable
    printf("Initiiial value of sharedVariable: %d\n", sharedVariable);

    // Attempt to modify the shared variable
    modifySharedVariable();

    // Display the modified value of the shared variable
    printf("Modified value of shharedVariable: %d\n", sharedVariable);

    return 0;
}


/*int main()
{
    printf("Hello World");
    //alternate_swap(0xad56);

    return 0;
}
*/


  ```
