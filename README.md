smsAuth
=======

An SMS based authentication system


#include<stdio.h>


int getDigit(int N,int *intPtr){

        int tempDigit =0;
       while(N!=0){
           tempDigit++;
       N=N/10;
      }
        *intPtr = tempDigit;
        return 0;
}

int GetLen(int N,int *ret){
        *ret=0;
        int tN=N;
        tN=(tN>=0)?tN:(-tN==N?-1:-tN);
        if(tN==0){ *ret=1; return 0;}
        return (tN>=0)?(getDigit(tN,ret)):-1;

}

int main(){


        int res=0;
        int x1=0;
        int val=2147483647;
        int nval=-2147483648;
        int nval1=-12349876;

        printf("%ld\n",sizeof(int));
        x1=GetLen(val,&res);
        printf("%d %d\n",res,x1);
       x1=GetLen(nval,&res);
        printf("chk %d %d\n",res,x1);
       x1=GetLen(-0,&res);
        printf("%d %d\n",res,x1);
        x1=GetLen(0,&res);
        printf("%d %d\n",res,x1);
       x1=GetLen(nval1,&res);
        printf("%d %d\n",res,x1);

}
