#include <bits/stdc++.h>
using namespace std;
int max_adj_Diff(int A[],int size){
   int MaxD=A[1]-A[0];
   for(int i=1;i<size-1;i++){
      if(A[i+1]-A[i] > MaxD)
         MaxD=A[i+1]-A[i];
   }
   return MaxD;
}
int main(){
   int a=1,b=2,c=3,d=4,e=5,f=6,g=7;
   int Arr[]={a,b,c,d,e,f,g};
   int md=max_adj_Diff(Arr,7);
   if (md==1)
   cout<<"Equal difference";
   else
   cout<<"Unequal difference";
   return 0;
}
