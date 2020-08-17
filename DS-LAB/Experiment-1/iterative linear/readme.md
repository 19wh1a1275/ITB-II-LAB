#	LINEAR SEARCH

## AIM OF THE EXPERIMENT:

### To perform linear search on the given array.

#### DESCRIPTION:

We use linear search to find whether a number is present in an array.
If it is present, then at what location it occurs.
It is also known as a sequential search.
It is straightforward i.e., we compare each element with the element to search until we find it or the list ends.

#### PROCEDURE:

#include<stdio.h>

int LinearSearch(int [],int,int);

int main()

{

int i,position,key;

int a[10] = {3,6,8,10,14,15,20,30,66,99};

scanf("%d",&key);

position = LinearSearch(a,10,key);

if (position == -1){

printf("Search is Unsuccessful");

}

else {

printf("Search is successful at position %d",position);

}

return 0;

}

int LinearSearch(int a[],int n,int key)

{

int i;

for (i = 0;i < n ; i++){

if (a[i] == key){

return i;

}

}

return -1;

}

Array : {10,6,8,15,20,3,14,99,66,30}

OUTPUT 1 [KEY ELEMENT = 66]:

We check each element of the given array against the given key element is 66
When the search reaches 8th element, the element is matched with the key element, therefore, the search ends here. Thus, the position obtained is ’8’.

OUTPUT 2 [KEY ELEMENT = 0]:

We check each element of the given array against the given key element is 0
The search reaches the last element of the array but as no element is matched the search ends here. Therefore, the search is unsuccessful as the element is not present. 

![output] 







