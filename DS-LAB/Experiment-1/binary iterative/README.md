# BINARY SEARCH

## AIM OF THE EXPERIMENT

To perform the BINARY SEARCH on a given array.
### DESCRIPTION:

Binary search algorithm applies to a sorted array for searching an element .
In case the target element is less than the middle element of the array then the second half of the array is discarded and the search continues by dividing the first half.

#### PROCEDURE:  

#include<stdio.h>

int BinarySearch(int [],int,int,int);

int main()

{

int i,key,position;

int a[10] = {3,6,8,10,14,15,20,30,66,99};

scanf("%d",&key);

position = BinarySearch(a,0,10,key);

if (position == -1){

printf("Search is Unsuccessful"); }

else{

printf("Search is successful at position %d",position); }

return 0;

}
int BinarySearch(int a[],int first,int last,int key)

{

int mid;

while(first <= last)

{

mid = (first + last ) / 2;

if (a[mid] == key)

return mid;

else if (key > a[mid])

first = mid + 1;

else

last = mid - 1;

}

return -1;

}

Given Array is: {10,6,8,15,20,3,14,99,66,30}

The sorted Array is: {3,6,8,10,14,15,20,30,66,99 }

OUTPUT 1 [KEY ELEMENT = 6]:

Step 1 :- First index = 0, last index = 9, mid index = 4
a[4]=14 and  14 < a[4].

Step 2 :- First index = 0, last index = 3, mid index = 1
a[1] = 6  and a[1] = 6.

OUTPUT 2 [KEY ELEMENT = 14]:

Step 1:- First index =0, last index = 9, mid index = 4
a[4]= 14  and  a[4] < 51.

Step 2 :-First index = 5, last index = 9,mid index = 7
a[7] = 30 and a[7] < 51.

Step 3 :-First index = 4, last index = 9, mid index = 4
a[4] = 14 and a[4] = 14.

OUTPUT 3 [KEY ELEMENT = 99]:

Step 1 :-First index = 0, last index = 9, mid index = 4
a[4]  = 14 and a[4] > 51.

Step 2 :-First index = 0, last index = 3 , mid index = 1
a[1] = 6 and a[1] < 51.

Step 3 :-First index  = 2, last index = 3, mid index = 2
a[2] = 8 and a[2] < 51.

Step 4 :-First index = 9, last index = 9, mid index = 9
a[9] = 99 and a[9] = 99.


