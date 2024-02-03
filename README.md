#include<iostream>
using namespace std ;
// Using Dutch National Flag Algorithm. 
void swap(int &a, int&b){
  int temp=a;
  a=b;
  b=temp ;
}
void MoveLeftToRight(int *arr,int n){ 
  int low =0,high = n-1; 
  while(low<high){ 
  if(arr[low]<0){ 
    low++; 
  }else if(arr[high]>0){ 
    high--; 
  }else{ 
    swap(arr[low],arr[high]); 
  } 
  } 
} 

int main() { 
  // Data 
  int arr[] = {1, 2, -5, 2, -7, 3, 2, -6, 3, 2, 1}; 
  int n = sizeof(arr)/sizeof(int); 
  MoveLeftToRight(arr,n); 
//printing array
  for(int i=0;i<n;i++){ 
    cout<<arr[i]<<" "; 
  } 
  return 0; 
} 
