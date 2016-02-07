#include<stdio.h>
#include<stdlib.h>
#include<time.h>

bool fim = false;

int main()
{
    int n,m,a,me,q;
    char move; 
    char e[] = "* ";
    
    int  matriz[5][5];
    srand((unsigned) time(NULL));
    a = (rand() % 14) + 1;
    me = (rand() % 14) + 1;
    
    while(!fim)
    {
    for(n=0;n<=11;n++)
    {
        for(m=0;m<=16;m++)
        {
            if(n==11 && m==a)
            {
                printf("@");
            }
            else if(n==1 && m==me)
            {
                printf("%c", &e);
            }
            else if(n==0 || n==11)
            {
                printf("——");
            }
            else if(m==0 || m==16)
            {
                printf("|");
            }
            else
            {
            printf("  ");
            }
            
        }
        printf("\n");
    }
        
    scanf("%i", &q);
       
        switch(q)
        {
            case 1:
            fim = true;
            break;
           case 2:
                system("clear");
                me++;
                break;
            
        }
        
    
     }
    
    return 0; 
}
