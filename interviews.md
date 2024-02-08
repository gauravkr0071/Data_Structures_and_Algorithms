1. how to create a process
2. what happens when a process accessing the critical section
 locked by mutex  and a interrupt comes to acces that critical section
3. convert a hexadecimal number contaiine in int x=0x45678923 into float euivalent
4. can you swap a nibble in hexadecimal int x= 0x5678 to x =0x7856
5. what is diifernce between semaphore and mutex or binary semaphore and mutex
6. differnce between const int * ptr , int const *ptr
7. what will x will contain, int *x=(int*) malloc(10) , how much size is allocated
8. tell me size of struct A{int a; int b; char c;}
9. tell me size of struct B{int a;  char c; int b;}
10. how to pack struct B
11. define a macro for sqauring, #define square(x) x*x, wha will happen if i pass , square(2+3)
12. can you toogle a specific bit without xor and for loop
13.  fork() ; cout <<"hello world" ; fork() fork() cout<< "HI";
14.  int x=5; tell me, *x++, *++x, ++*x;
15.  where const varibles are stored and string literals are stored

```c
#include <stdio.h>

int swapHexBytes(int x) {
    int numBytes = sizeof(int); // Number of bytes in an integer
    int swapped_x = 0;

    // Swap bytes using bitwise operations
    for (int i = 0; i < numBytes / 2; i++) {
        // Extract bytes to swap
        int byte1 = (x >> (i * 8)) & 0xFF;
        int byte2 = (x >> ((numBytes - 1 - i) * 8)) & 0xFF;

        // Swap bytes
        swapped_x |= (byte2 << (i * 8)) | (byte1 << ((numBytes - 1 - i) * 8));
    }

    return swapped_x;
}

int main() {
    int x = 0x12345678; // Example hexadecimal number
    int swapped_x = swapHexBytes(x);

    printf("Original value of x: 0x%X\n", x);
    printf("Swapped value of x: 0x%X\n", swapped_x);

    return 0;
}

```
   
