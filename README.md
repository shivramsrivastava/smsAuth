smsAuth
=======

An SMS based authentication system
ubuntu@ip-172-31-16-41:~/ctest$ cat getLen.c
#include<stdio.h>


int GetLen(int N,int *ret){

        int retErroCode=1;
        int retSuccessCode=0;
        int digit =0;
        if(N==0){
                printf("retu");
                return retErroCode;
        }
        while((N/10)!=0){
                digit++;
                N=N/10;
        }

        *ret=digit;
        return retSuccessCode;
}

int main(){


        int res=0;
        int x1=0;
        int val=2147483647;
        int nval=-2147483648;

        printf("%ld\n",sizeof(int));
        x1=GetLen(val,&res);
        printf("%d %d\n",res,x1);
       x1=GetLen(nval,&res);
        printf("%d %d\n",res,x1);
       x1=GetLen(-0,&res);
        printf("%d %d\n",res,x1);
        x1=GetLen(0,&res);
       //x1=GetLen(123456789,&res);
        printf("%d %d\n",res,x1);

}
ubuntu@ip-172-31-16-41:~/ctest$ cat mysort.c
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
int mysort(int *arr,int len, int flag){

        if (flag == 0){
                qsort(arr,len, sizeof(int), moreFunc);
        }else{
                qsort(arr,len,sizeof(int),lessFunc);
        }

}


int print(int *arr, int len){

        int i=0;

        for(i=0;i<len;i++){
                printf("%d ",arr[i]);
        }
        printf("\n\n\n");

}

int main(){

        int xarr[5]={99,45,12,-9,1};
        int yarr[6]={99,45,12,-9,1,98};

        mysort(xarr,5,0);
        print(xarr,5);
        mysort(yarr,6,1);
         print(yarr,6);



}
