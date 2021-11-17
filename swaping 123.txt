//202115
#include<iostream>
void swapFunction1(int &n1,int &n2)
{
     int temp=n1;
     n1=n2;
     n2=temp;
}

void swapFunction2(int *n1,int *n2)
{
    int temp=*n1;
    *n1=*n2;
    *n2=temp;
}
using namespace std;
int main()
{
    int a=5, b=9;
//printing values of a and b after swap operation
    swapFunction1(a,b);
    cout<<"After swap with swapFunction1 values of a and b is:"<<endl;
    cout<<"a= "<<a<<endl<<"b= "<<b<<endl;
    swapFunction1(a,b);//swaping a and b to obtain original values
//printing values of a and b after swap operation with the swapFunction2
    swapFunction2(&a,&b);
    cout<<"After swap with swapFunction2 values of a and b is:"<<endl;
    cout<<"a= "<<a<<endl<<"b= "<<b<<endl;
    return 0;
}
