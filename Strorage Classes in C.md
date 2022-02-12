- https://www.geeksforgeeks.org/storage-classes-in-c/
- https://www.geeksforgeeks.org/storage-classes-in-c-with-examples/
-https://www.geeksforgeeks.org/memory-layout-of-c-program/?ref=lbp
- https://www.geeksforgeeks.org/dynamically-allocate-2d-array-c/?ref=lbp
```cpp
#include <stdio.h>
#include <stdlib.h>

int main()
{
	int r = 3, c = 4, i, j, count;

	int* arr[r];
	for (i = 0; i < r; i++)
		arr[i] = malloc(c * sizeof(int));

	// Note that arr[i][j] is same as *(*(arr+i)+j)
	count = 0;
	for (i = 0; i < r; i++)
		for (j = 0; j < c; j++)
			arr[i][j] = ++count; // Or *(*(arr+i)+j) = ++count

	for (i = 0; i < r; i++)
		for (j = 0; j < c; j++)
			printf("%d ", arr[i][j]);

	/* Code for further processing and free the
	dynamically allocated memory */

	for (int i = 0; i < r; i++)
		free(arr[i]);

	return 0;
}
```
- https://www.geeksforgeeks.org/pass-2d-array-parameter-c/?ref=lbp
```cpp
If compiler is not C99 compatible, then we can use one of the following methods to pass a variable sized 2D array.
4) Using a single pointer 
In this method, we must typecast the 2D array when passing to function.
#include <stdio.h>
void print(int *arr, int m, int n)
{
    int i, j;
    for (i = 0; i < m; i++)
      for (j = 0; j < n; j++)
        printf("%d ", *((arr+i*n) + j));
}
 
int main()
{
    int arr[][3] = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
    int m = 3, n = 3;
 
    // We can also use "print(&arr[0][0], m, n);"
    print((int *)arr, m, n);
    return 0;
}
Output
1 2 3 4 5 6 7 8 9 
```

```cpp
// The following program works only if your compiler is C99 compatible.
#include <stdio.h>
 
// n must be passed before the 2D array
void print(int m, int n, int arr[][n])
{
    int i, j;
    for (i = 0; i < m; i++)
      for (j = 0; j < n; j++)
        printf("%d ", arr[i][j]);
}
 
int main()
{
    int arr[][3] = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
    int m = 3, n = 3;
    print(m, n, arr);
    return 0;
}

```
