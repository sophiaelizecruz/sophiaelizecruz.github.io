---
layout: essay
type: essay
title: Ask, And You Shall Receive
# All dates must be YYYY-MM-DD format!
date: 2020-01-23
labels:
  - Coding Style
  - Stack Overflow
  - Learning
  - C
---

## Be Careful What You Wish For.

Regardless of our skill level as software engineers, we all come to a point where we will need to ask others for help. However, that is only half the battle. The question is, _how_ do we ask for help? 

## What Constitutes A Smart Question? 

First of all, what _exactly_ are you trying to solve? 

By knowing what exactly you want to solve, it saves you a lot of time. There are threads from users that might have had the 
same problem with their software or hardware! The internet is your friend. There are also many online resources available to 
us, from Stack Overflow to the humble FAQ. It also helps to browse forums and threads that may be similar to your problem 
before asking; it may even answer your question! There are many tools such as tags that can help 
someone narrow down their search. You can experiment on your own or ask people that you know who you think would be 
knowledgable on the topic. It's only after your research that you should consider asking people online for help if your search 
does not produce the answers you need. Asking the developer should only be used as a last resort. 

By showing that you can take the time to do the research and that you can formulate a "smart" question, it also gives 
"hackers" the impression that you aim to maintain a level of professionalism, and that you do not intend to waste their time. 
This may even result in making connections with these "hackers" because you have proven that you are capable of 
such problem-solving skills, which may benefit your career in the long run.


## So, What Does A Smart Question _Look_ Like?
The following entry displays a ReactJS related question, where the 
user wanted to know how to activate a progress bar countdown after the pushing 
of a button to show the amount of time before the button was to be active again.

```
Q: I am trying to activate a progressbar 
countdown after I push abutton. 
So the button will be disabled for 90 seconds. 
After the progressbar arrived to 90, the button 
will be active again. How to do that?

Below is what I was able to achieve so far:

js:

class BoatMap extends Component {
    constructor(props) {
        super(props);
        this.state = {
            buttonEnabled: true
        };
        this.updateRequest = 
        this.updateRequest.bind(this);
    }

    updateRequest() {
        const url =
            'html request for API';
        console.log(url);
        fetch(url, fetchConfig)
            .then((jsonObject) => {
                // fetching data
              })
            });
        this.setState({
            buttonEnabled: false
        });
        setTimeout(() => {
            this.setState({ buttonEnabled: true });
        });
    }

    render() {
        return (
            <div className="google-map">
                <GoogleMapReact>
                    <div class="progress-circle p0">
                        <span>0%</span>
                        <div class="left-half-clipper">
                            <div class="first50-bar" />
                            <div class="value-bar" />
                        </div>
                    </div>
                    <button className=
                    "btn-next-request" onClick={() 
                    => this.updateRequest()}>
                        Time to Next API Request
                    </button>
                </GoogleMapReact>
            </div>
        );
    }
}
What I have done so far:

1) I came across the following source but was not able 
to figure out how to implement it yet.

2) This post is a good source too. 
However I am not sure about the 
approach it was taken. Despite that, I was able 
thanks to that post to set the button call. 
I can confirm that the button 
is correctly functioning 
and sending the request.

3) In addition this is another good source, 
although it is using jquery. I am not very familiar with 
jquery but this could be a good approach. 
However, I would prefer not to mix too many things.

Thanks for pointing in the right 
direction to solve 
this problem.

```

The user starts by stating the problem and the goal that they have for their code, and they provide their code in a way that is easy to read. They also list the measures that they had taken to figure out their problem before posting to Stack 
Overflow, such as linking the posts that they had gone to, as they had included links to the sites that they had gone on. 
There are some grammatical errors, and while there could have been some parts that the user could have specified further, the post is formatted nicely and is easy to read. It is a decent question, which in turn, allowed this user to get the answer that they needed. 

## A: STFW!

The following entry displays a user that had asked for help regarding their C program in which their goal was to read in data from a file, but they were having trouble reading in the file's contents and had mentioned that they were reading in random characters.

``` 
Q: Hello so i am creating a 
program that 
reads from a file and outputs 
each category of the things in 
the text in sorted for 
example i want it to output like this :

Company name: air france 
Date of creation: 06281957 Flight number: AT6801 
Incoming city: london Arrival city: paris Amount of 
fuel liters left: 380 Plane category: B777
this is the input :

air qatar06281957AT680londonmadrid380B777 
turkish airlines052019
33TK1298istanbulmadrid250A380 
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
    int i,j,c=0,l,c2=0,c3=0;
    int c4=0;int c5=0,c6=0,k,m,c7=0,flag=0;int 
    c8=0,c9=0,c10=0,
    flag2=0,n,c11=0,c12=0,c13=0,c14=0,p=0,
    c15=0,c16=0,t,t1,t2,t3,t4,t5,t6,t7,s;
    char ultimate_array[600];
    char plane[100][6];
    char date[600][6];
    char nflight[600][6];
    char  destination[100][6];
    char fuel[100][6];
    char planetype [100][6];

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
                    destination[t][c7]=
                    ultimate_array[m];
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
                    fuel[t][c11]=
                    ultimate_array[n];
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
                    planetype[t][c16]=
                    ultimate_array[p];
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

I have been struggling with a lot of things 
but I finally managed to separate every 
category to a different array, however ,
when I tried to do it for 2D array 
I always get garbage can someone point out 
what the mistake I did ?

we couldn't read in the input file and write it 
in a 2D array so the concept that i 
have used in this code i search in the array until 
i find something that would help 
me separate the word from the others such as 06281957 
in the input i used isdigit 
to identify which index has it then i copy 
the previous characters into a new array 
this trick seemed to work for a 1d array however 
when i tried to scan it to 2d it stopped 
working and only random chars seemed to appeari 
wanted to print the whole 2d 
array of each category but i failed to 
do so, for the variables i used them as 
checkpoints for the next check to put the things 
i want in a new array. 
For minimizing the code i cant seem to find another 
solution to do so i know that my code is 
very big but if someone has a better idea it would be awesome.
    
```

Many things would prompt others to avoid helping this user. The first few replies to this post are asking the user to specify 
the problem that they are having with their code, and for the user to read the help pages regarding how to ask a "good" 
question. 

This user provides _way_ too much code, and the user should have condensed the problem area so that it would be easier for 
other users to understand the problem that he/she is having. They state that they "always get garbage" but don't elaborate on 
it. What do they mean by "garbage"? However, they elaborate on this later on, but when they do, it's lost in the sea of the 
next paragraph. Furthermore, the structure and flow of their post are also very messy, as it lacks proper grammar and 
punctuation. What the user could have done is that they could have traced the code to figure out a possible problem area, and 
at the very least, should have provided test code to help the "hackers" understand where their code is going wrong. It would 
also help if the user had stated what measures they took to solve the problem. Overall, this entry makes the original poster 
seem lazy and could reduce the chances of them getting help from "hackers" in the future.

## The Takeaway

After this experience, I feel that I have a boilerplate for constructing smarter questions. Before reading Raymond's essay on 
the etiquette of asking "smart" questions, I had been unsure of how to approach my professors or a TA for help in fear that it 
would sound mindless and that it would waste their time. Asking a smart question should not be that intimidating. It is a 
matter of preparation, for taking the time to think about what you want to ask about. By practicing this formula for smart 
questions, this will not only benefit me during my college career but in later endeavors.
