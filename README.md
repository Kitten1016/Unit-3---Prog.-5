#include <stdio.h>

#include <math.h>



float calcCharge (float);



int main()

{

    float hours1 =0.0;

    float hours2 =0.0;

    float hours3 =0.0;

    float charge1 =0.0;

    float charge2 =0.0;

    float charge3 =0.0;

    float totalHours =0.0;

    float totalCharge =0.0;


    printf ("Enter the hours for car 1:\t");

    scanf ("%f", &hours1);

    printf ("\nEnter the hours for car 2:\t");

    scanf ("%f", &hours2);

    printf ("\nEnter the hours for car 3:\t");

    scanf ("%f", &hours3);



totalHours = hours1 + hours2 + hours3;

    

    charge1 = calcCharge (hours1);

    charge2 = calcCharge (hours2);

    charge3 = calcCharge (hours3);



totalCharge = charge1 + charge2 + charge3;


    
printf ("\nCar\tHours\tCharge");

    printf ("\n1\t% 0.1f\t% 0.2f", hours1, charge1);

    printf ("\n2\t% 0.1f\t% 0.2f", hours2, charge2);

    printf ("\n3\t% 0.1f\t% 0.2f", hours3, charge3);

    printf ("\nTotal\t% 0.1f\t% 0.2f\n\n", totalHours, totalCharge);

} 

float calcCharge (float hours)
{

    float cHours = ceil(hours);

    float charge = 0.0;

    

    if (cHours <= 3.0)

    charge = 2.00;

    else if (cHours > 3.0 && cHours <= 17.0)

    charge = ( (cHours - 3.0)* 0.5) + 2.0;

    else

    charge = 10.0;


    
    return charge;


}
