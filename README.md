smsAuth
=======

An SMS based authentication system


#include <stdlib.h>
#include "oj.h"



int getDigit(int N,int *intPtr){

	int tempDigit=0;
	while(N!=0){
		tempDigit++;
		N=N/10;
	}
	*intPtr = tempDigit;
	return 0;
}

int GetNumLenth(int inputNum, int *pNumLenth){
        *pNumLenth=-1;
        int tN=inputNum;
        tN=(tN>=0)?tN:(-tN==inputNum?-1:-tN);
        if(tN==0){ *pNumLenth=1; return 0;}
        return (tN>0)?(getDigit(tN,pNumLenth)):-1;

}

