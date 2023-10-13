# Quadratic-Equation-Roots
The program takes coefficients of quadratic equation as input and outputs roots of the equation.
<br>
#include<stdio.h>
<br>
#include<conio.h>
<br>
#include<math.h>
<br>
void main()
<br>
{
<br>
    float a,b,c,d,x,xreal,ximg,alpha,beta;
    <br>
    printf("\n enter the coefficients of quadratic equation a,b and c \n");
    <br>
    scanf("%f %f %f", &a,&b,&c);
    <br>
    if (a==0)
    <br>
    {
    <br>
        printf("not a Q.E.");
        <br>
        if (b!=0)
        <br>
        {
        <br>
            x<- -c/b;
            <br>
            printf ("x=%f",x);
            <br>
        }
        <br>
        else 
          {
            d=b*b-(4*a*c);
            if(d>0)
            {
                printf("roots are real and distinct");
                alpha= -b + sqrt (d)/(2*a);
                beta = -b - sqrt (d)/(2*a);
            }
            if (d==0)
            {
                printf("roots are real and distinct \n");
                alpha = -b/(2*a);
                beta = alpha;
            }
            printf("roots of QE are x1=%f and x2=%f", alpha,beta);
        }
    }
        else
        {
            printf("roots are complex or imaginary");
            xreal= -(b/(2*a));
            ximg= -(sqrt(d)/(2*a));
            printf("first complex root = %f+i%f", xreal,ximg);
            printf("second complex root = %f-i%f", xreal,ximg);

        }
        getch();
    }


