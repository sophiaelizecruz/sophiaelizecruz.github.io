---
layout: essay
type: essay
title: Ask, And You Shall Receive
# All dates must be YYYY-MM-DD format!
date: 2020-01-23
labels:
  - Coding Style
  - Stack Overflow
---

## But be careful what you wish for.

Regardless of our skill level as software engineers, we all come to a point where we will need to ask others for help. However, that is only half the battle. The question is, _how_ do we ask for help? 

Smart questions made up of knowing exactly what you want, doing research, using manners, 
Need smart questions as it reflects your capabilites such as initiative, willingness to learn, problem solving skills
Mutual thing - helps us to grow and improve together
Make connects from these encounters
Shows off your professionalism

``` 
Hello so i am creating a program that reads from a file and outputs each category of the things in the text in sorted for 
example i want it to output like this :

Company name: air france Date of creation: 06281957 Flight number: AT6801 
Incoming city: london Arrival city: paris Amount of 
fuel liters left: 380 Plane category: B777
this is the input :

air qatar06281957AT680londonmadrid380B777 
turkish airlines05201933TK1298istanbulmadrid250A380 
lufthansa01061953LH29frankfurtmadrid75B747 
air canada06281957AT7245ammanmadrid120A320 
turkish airlines05201933TK1266dohamadrid522A320 
air france10071933AF123parismadrid105B777 -1

The code:

#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main()
{
    FILE *inp,*outp;
    int i,j,c=0,l,c2=0,c3=0;int c4=0;int c5=0,c6=0,k,m,c7=0,flag=0;int 
    c8=0,c9=0,c10=0,flag2=0,n,c11=0,c12=0,c13=0,c14=0,p=0,
    c15=0,c16=0,t,t1,t2,t3,t4,t5,t6,t7,s;
    char ultimate_array[600];char plane[100][6];
    char date[600][6];char nflight[600][6];
    char  destination[100][6];
    char fuel[100][6];char planetype [100][6];

    inp=fopen("input.txt","r");

    for(i=0;!feof(inp);i++)
    {
        fscanf(inp,"%c",&ultimate_array[i]);
    }

    s=strlen(ultimate_array);

    for(i=0;i<s;i++)
    {
        printf("%c",ultimate_array[i]);
    }

    printf("\n\n\n\n\n\n\n\n\n\n\n\n");
    for(t=0;t<6;t++)
    {
        for(j=0;j<200;j++)
        {
            c++;
            if(isdigit(ultimate_array[j]))
            {
                c3=c;
                while(c>=0)
                {
                    plane[t][c]=ultimate_array[j];
                    c--; j--;
                }
                break;
            }
        }

        for(k=0;k<200;k++)
        {
            c2++;
            if(isupper(ultimate_array[k]))
            {
                c5=c2; c2=c2-c3; c9=c2;
                while(c2>=0)
                {
                    date[t][c2]=ultimate_array[k];
                    k--; c2--;
                }
                break;
            }
        }

        for(l=c3;l<200;l++)
        {
            c4++;
            if(islower(ultimate_array[l]))
            {
                c4=c4+c3-c5;
                while(c4>=0)
                {
                    while(flag==0)
                    {
                        c8=c4; c6=c4+c5; flag=1;
                    }

                    nflight[t][c4]=ultimate_array[l];
                    c4--; l--;
                }
                break;
            }
        }

        c10=c9+c8;

        for(m=c6;m<200;m++)
        {
            c7++;
            if(isdigit(ultimate_array[m]))
            {
                c7--;m--;

                while(c7>=0)
                {
                    while(flag2==0)
                    {
                        c13=c7; flag2=1;
                    }
                    destination[t][c7]=ultimate_array[m];
                    c7--; m--;
                }
                break;
            }
        }

        for(n=c14;n<200;n++)
        {
            c11++; c14=c3+c13+c10;
            if(isupper(ultimate_array[n]))
            {
                c12=c11; c11=c11-1;
                while(c11>=0)
                {
                    fuel[t][c11]=ultimate_array[n];
                    c11--; n--;
                }
                break;
            }
        }

        c15=c14+c12;

        for(p=c15;p<200;p++)
        {
            c16++;
            if(ultimate_array[p]=='\n')
            {
                while(c16>=0)
                {
                    planetype[t][c16]=ultimate_array[p];
                    c16--; p--;
                }
                break;
            }
        }

        for(t1=0;t1<20;t1++)
        {
            printf(" %c",plane[t1][t]);
        }

        printf("\n");

        for(t2=0;t2<100;t2++)
        {
            printf("%c",destination[t2][t]);
        }

        printf("\n");

        for(t3=0;t3<100;t3++)
        {
            printf("%c",date[t3][t]);
        }

        printf("\n");

        for(t4=0;t4<100;t4++)
        {
            printf(" %c",fuel[t4][t]);
        }

        printf("\n");

        for(t5=0;t5<100;t5++)
        {
            printf(" %c",nflight[t5][t]);
        }
        printf("\n");
        for(t6=0;t6<5;t6++)
        {
            printf(" %c",planetype[t][t6]);
        }
    }

    return 0;
}

I have been struggling with a lot of things but I finally managed to separate every 
category to a different array, however ,when I tried to do it for 2D array 
I always get garbage can someone point out what the mistake I did ?

we couldn't read in the input file and write it in a 2D array so the concept that i 
have used in this code i search in the array until i find something that would help 
me separate the word from the others such as 06281957 in the input i used isdigit 
to identify which index has it then i copy the previous characters into a new array 
this trick seemed to work for a 1d array however when i tried to scan it to 2d it stopped 
working and only random chars seemed to appeari wanted to print the whole 2d 
array of each category but i failed to do so, for the variables i used them as 
checkpoints for the next check to put the things i want in a new array. 
For minimizing the code i cant seem to find another solution to do so i know that my code is 
very big but if someone has a better idea it would be awesome.
    
```
There are many things that would prompt others to avoid helping this user. This user provides way too much code, and should have condensed the problem area so that it would be easier for other users to understand the problem that he/she is having. What they could have done is that they could have traced the code to figure out a possible problem area, and at the very least, should have provided test code to help the "hackers" understand where their code is going wrong. It would also help if the user had stated what measures they took to solve the problem. 

The structure and flow of their post is also very messy, lacking proper grammar and punctuation. They state that they "always get garbage" but don't elaborate on it, and when they do, it's lost in the sea of the next paragraph. 

After reading this, have a boilerplate as to how I can construct smarter questions
Always panic trying to think of one, so have to step back and think
Especially when asking professors, since they also have things to do
Don't waste others time
Is a good way to exercise other soft skills

