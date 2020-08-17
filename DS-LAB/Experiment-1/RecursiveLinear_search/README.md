
#	LINEAR SEARCH WITH RECURSION

## AIM OF THE EXPERIMENT:                                                                              

### To perform LINEAR SEARCH on a given array using  RECURSION.

#### DESCRIPTION:

We use linear search to find whether a number is present in an array .

If it is present, then at what location it occurs.

We use recursive function to search the key element in the array.

#### ROCEDURE: 

#include<stdio.h>

int ReLinearSearch(int [],int,int);

int main()

{

int i,position,key;

int a[10]= {3,6,8,10,14,15,20,30,66,99};

scanf("%d",&key);

position = ReLinearSearch(a,10,key);

if (position == -1){

printf("Search is unsuccessful");

}

else{

printf("Search is successful at position %d",position);

}

return 0;

}

int ReLinearSearch(int a[],int n,int key)

{

if (n > 0){

if(a[n - 1] == key){

return n-1;

}

else {

return ReLinearSearch(a,n-1,key);

}

}

return -1; 

}

Array : {10,6,8,15,20,3,14,99,66,30}

OUTPUT 1 [KEY ELEMENT = 66]:

We check each element of the given array against the given key element is 66
When the search reaches the 8th element, the element is matched with key element therefore, the search ends here. Thus, the position is obtained i.e.,’8’.

OUTPUT 2 [KEY ELEMENT = 0]:

We check each element of the given array against the given key element is 0.
The search reaches the last element of the array but as no element is matched the search ends here. Therefore, the search in unsuccessful as the element is not present.
	
	![output]

