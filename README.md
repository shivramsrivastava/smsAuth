smsAuth
=======

An SMS based authentication system


#define MIN(a,b) (a<b?a:b)

void getNumber(unsigned int first, unsigned int second, unsigned int *pHighCommonDivissor, unsigned int *pLeastCommonMultiple)
{

        unsigned int i=MIN(first,second)/2;
        for(;i>0 && ( first%i || second%i);--i);
        *pHighCommonDivissor=i;
        *pLeastCommonMultiple=((first*second)/i);
        return;
}
