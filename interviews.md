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

__Broadcom Interview __
- print int x= 12345, in 12345 order means 1 then 2 then 3 then 4 then 5, but in one pass only , ans: recursive
- find the nth node from last, in one pass , ans: recursion
- print the node in reverse order, ans recursion
- swap the alternate bits of a number
```cpp
// 1001 1110 0001 1010
//  9    e    1  a
// 0110 1101 0010 0101
//   6 d 2 5
int swap(int x)
{
    int a= x & 0xAAAA;
        a=a>>1;
    int b= x & 0x5555    ;
        b=b<<1;
    
    //printf("%d",a|b);
    
    return a|b;
    
}    
```

- 2 identical eggs , and a biludilng of 100 floor, find the max floor fromm whcih it willl not break, make a algo
  you can break the eggs only one time and reach the answer 
- find the count set bits in a number in a constant time (i ahve solved in O(number of set bits))
- find the sub array which have sum zero and return ots starting and end index
- what is volatile and register keyword ?
- can we do something like const volatile ? what is that ?
- a array of size 100 contains num 0 to 99 , one is missing , in random order , and one is repateted two times, find the missing number
- how device tree works
- what is platform driver
- how a kernel knows what is connected and which device is there 
- what is interconnect
- can you extract bits from n to m in constant time
- find the common node in a Y shaped linked list in one pass , ans: recursion
- suppose i want to pass "hello world " string to a device from kernel , how i can do that,
- differnce betwwen semaphore and mutex 
```
   
