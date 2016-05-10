smsAuth
=======

An SMS based authentication system


#include<stdio.h>
#include<stdlib.h>


int moreFunc(const void * a, const void * b)
{
   return ( *(int*)a - *(int*)b );
}

int lessFunc(const void * a, const void * b)
{
   return ( *(int*)b - *(int*)a );
}

typedef int (*cmpfunc)(const void *, const void*);
cmpfunc funcarray[2]={moreFunc,lessFunc};

int mysort(int *arr,int len, int flag){

        if (flag == 0 || flag==1){
                qsort(arr,len, sizeof(int), funcarray[flag]);
        }
        return;
}


int print(int *arr, int len){

        int i=0;

        for(i=0;i<len;i++){
                printf("%d ",arr[i]);
        }
        printf("\n\n\n");

}

int main(){

//funcarray[0]=moreFunc;
//funcarray[1]=lessFunc;


        int xarr[5]={99,45,12,-9,1};
        int yarr[6]={99,45,12,-9,1,98};

        mysort(xarr,5,0);
        print(xarr,5);
        mysort(yarr,6,1);
         print(yarr,6);



}



#include <stdlib.h>
#include "oj.h"



int GetNumLenth(int inputNum, int *pNumLenth){

        if(pNumLenth!=NULL){
        *pNumLenth=1;
         while((inputNum/10)!=0){
                ++*pNumLenth;
                inputNum=inputNum/10;
        }
                return 0;
        }
        return -1;
}



