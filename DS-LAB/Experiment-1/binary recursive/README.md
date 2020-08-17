#	BINARY SEARCH WITH RECURSION

## AIM OF THE EXPERIMENT:
To perform BINARY SEARCH on a given array using  RECURSION.

### DESCRIPTION:
Binary search algorithm applies to a sorted array for searching an element .
In case the target element is less than the middle element of the array then the second half of the array is discarded and the search continues by dividing the first half. We use recursive function to search the key element in the array. 

#### PROCEDURE:

#include<stdio.h>

int ReBinarySearch(int[],int,int,int);

int main()

{

int key,i,position;

int a[10] = {3,6,9,10,14,15,20,30,66,99 };

scanf("%d",&key);

position = ReBinarySearch(a,0,10,key);

if (position == -1){

printf("Search is unsuccessful"); }

else {


printf("Search is successful at position %d\n",position); }

return 0;

}

int ReBinarySearch(int a[],int first,int last ,int key)

{

int mid;

if (first <= last){

mid = (first + last) / 2;

if (a[mid] == key)

return mid;

else if (key > a[mid])

return ReBinarySearch(a,mid + 1,last,key);

else

return ReBinarySearch(a,first,mid - 1,key);

}

return -1; 

}

Given array is: {10,6,8,15,20,3,14,99,66,30}

The sorted Array is: {3,6,8,10,14,15,20,30,66,99}       

OUTPUT 1 [KEY ELEMENT =6]:

Step 1 :- First index = 0, last index = 9 , mid index = 4
a[4] = 14 and a[4] < 51.

Step 2 :- First index = 0, last index = 3, mid index = 1
a[1] =6 .

OUTPUT 2 [KEY ELEMENT = 14]:

Step 1 :- First index = 0, last index =9 , mid index = 4
a[4]= 14 and  a[4] < 51.

Step 2 :- First index = 5, last index = 9, mid index =7
a[7] = 30 and a[7] < 51.

Step 3 :- First index = 0, last index = 9, mid index =4
a[4] = 14.

OUTPUT 3 [KEY ELEMENT = 99]:

Step 1 :- First index = 0, last index = 9, mid index = 4
a[4] = 14 and  a[4] <51.

Step 2 :- First index = 0, last index = 3, mid index = 1
a[1] = 6 and  a[1] <51.

Step 3 :- First index = 2 , last index = 3, mid index = 2
a[2] = 8 and  a[2] <51. 

Step 4 :- First index = 9, last index = 9, mid index = 9
a[9] = 99.
!output]

![binary6](https://user-images.githubusercontent.com/69747236/90371681-eded0c00-e08c-11ea-96b4-54d77f2b3895.JPG)

![binaryR14](https://user-images.githubusercontent.com/69747236/90371682-ef1e3900-e08c-11ea-871c-03da156baa37.JPG)

![binary99](https://user-images.githubusercontent.com/69747236/90371684-efb6cf80-e08c-11ea-8907-5862ff90c1f5.JPG)

