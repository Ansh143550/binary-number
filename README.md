// binary-number
#include<iostream>
using namespace std;
int binarysearch(int arr[],int size,int key){
int start = 0;
int end = size-1;
int mid = start +(end-start)/2;
 while (start<=end){
  if (arr[mid]== key){
  return mid;
  }
  if (key>arr[mid]){
  start=mid+1;
  }
  else{  //key<arr[mid]
  end=mid-1;
  }
  mid=start +(end-start)/2;
  }
  return -1;
  }

  int main() {
   int even[6]={5,8,11,17,25,70};
   int odd[5]={3,10,14,15,20};

 int evenindex=binarysearch(even,6,25);
 cout << "index of 25 is " <<evenindex << endl;
 
 int oddindex=binarysearch(odd,5,3);
 cout << "index of 3 is " <<oddindex << endl;
 
 return 0;
   }
  
