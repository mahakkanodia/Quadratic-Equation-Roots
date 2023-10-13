# Quadratic-Equation-Roots
The program takes coefficients of quadratic equation as input and outputs roots of the equation.
#include<stdio.h>
#include<conio.h>
#include<math.h>
void main()
{
    float a,b,c,d,x,xreal,ximg,alpha,beta;
    printf("\n enter the coefficients of quadratic equation a,b and c \n");
    scanf("%f %f %f", &a,&b,&c);
    if (a==0)
    {
        printf("not a Q.E.");
        if (b!=0)
        {
            x<- -c/b;
            printf ("x=%f",x);
        }
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


