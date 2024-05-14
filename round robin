#include <stdio.h>
#define n 10

int main()
{
    int i, q, nop,j;
    float AT[n], BT[n], TAT[n], WT[n], BT1[n], c = 0, d = 0, x, y, w = 0;

    // number of processes
    printf("Enter number of processes: ");
    scanf("%d", &nop);

    // arrival time
    for (i = 0; i < nop; i++)
    {
        printf("Enter arrival time for process %d: ", i + 1);
        scanf("%f", &AT[i]);
    }

    // burst time
    for (i = 0; i < nop; i++)
    {
        printf("Enter burst time for process %d: ", i + 1);
        scanf("%f", &BT[i]);
        BT1[i] = BT[i];
    }

    // quantum
    printf("Enter quantum: ");
    scanf("%d", &q);

    // Round Robin
    c = 0;
    i = 0;
    j=nop;
    while (j != 0 )
  { 
      for(i=0;i<nop;i++)
    {  
        if(AT[i]>c)
        {
            c=AT[i];
        }
        if (BT1[i] > q)
        {
            c = c + q;
            BT1[i] = BT1[i] - q;
        }   
        else
        { if(BT1[i]>0)
        {
        
            c = c + BT1[i];
            BT1[i] = 0;
            TAT[i] = c - AT[i];
            WT[i] = TAT[i] - BT[i];
            j--;
        }
        }



    }
    }
        
    

    // Print Turn Around Time
    for (i = 0; i < nop; i++)
    {
        printf("The turn around time for process %d is %f\n", i + 1, TAT[i]);
    }

    // Print Waiting Time
    for (i = 0; i < nop; i++)
    {
        printf("The waiting time for process %d is %f\n", i + 1, WT[i]);
    }

    // Average Turn Around Time
    for (i = 0; i < nop; i++)
    {
        d = d + TAT[i];
    }
    x = d / nop;
    printf("Average Turn Around Time: %f\n", x);

    // Average Waiting Time
    for (i = 0; i < nop; i++)
    {
        w = w + WT[i];
    }
    y = w / nop;
    printf("Average Waiting Time: %f\n", y);

    
}
