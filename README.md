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




###################

#include<stdio.h>


unsigned int rabbitN(unsigned int x){
        unsigned int allArr[47]={1,1,2,3,5,8,13,21,34,55,89,144,233,377,610,987,1597,2584,4181,6765,10946,17711,28657,46368,75025,121393,196418,317811,514229,832040,1346269,2178309,3524578,5702887,9227465,14930352,24157817,39088169,63245986,102334155,165580141,267914296,433494437,701408733,1134903170,1836311903,
2971215073};

        return allArr[x];
}




int main(){

        unsigned int xval=4294967295,ret;
        int i;

        for(i=1;i<48;i++){
                ret=rabbitN(i);
                printf("%u\n",ret);
        }


        return 0;

}

