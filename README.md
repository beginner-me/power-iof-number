# power-iof-number
power of number
/* Write a C Program to Find Power of a Given Number Using Recursion */

/* OUTPUT: 
Enter a Value of Base: 2
Enter a Value of Power: 4
2 to the Power of 4 is : 16
*/
#include<stdio.h>
int main()
{
    int power(int x, int y);
    int a,b,res;
    printf("enter base number : ");
    scanf("%d",&a);
    printf("Enter power : ");
    scanf("%d",&b);
    res = power(a,b);
    printf(" %d raised to %d is %d",a,b,res);

}
int power(int x , int y)
{
    if(x==0)
    {
        return 0;
    }
    else if(y==0)
    {
        return 1;
    }
    else if(y==1)
    {
        return x;
        
    }
    else if(x==1)
    {
        return 1;
    }
    else{
        return(x*power(x,y-1));
    }
}
