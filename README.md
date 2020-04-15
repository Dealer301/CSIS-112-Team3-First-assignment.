# CSIS-112-Team3-First-assignment.
Team project for "The Tortist and the Hair"
This is a basic blue print for "The Tortoise and the Hare" Team project; for Team 3 of Terrie Canon's CSIS 112 class.


#define CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <stdlib.h>
#include <time.h>

//function prototypes

void printInstructions(void);
void moveTortoise(int *turtle);
void moveHare(int *hare);
void printCurrentPosition(int turtle, int hare);
void results(int turtle, int turtletime, int hare, int haretime, int timer);

int main(void)
{
    srand(time(NULL));
    
    int turtle = 1, hare = 1, timer = 0, turtletime = 0, haretime = 0;
    
    printInstructions();
    
    while (turtle < 70 && hare < 70)
        {moveTortoise(&turtle);
            moveHare(&hare);
            printCurrentPosition(turtle, hare);
            timer++;
        }
    if (turtle >= 70 && hare < 70)
        {turtletime = timer;
        while (hare < 70)
            {moveHare(&hare);
            printCurrentPosition(turtle, hare);
            timer++;
            }
        haretime = timer;
        }
    if (turtle < 70 && hare >= 70)
        {haretime = timer;
        while (turtle < 70)
            {moveTortoise(&turtle);
            printCurrentPosition(turtle, hare);
            timer++;
            }
        turtletime = timer;
        }
    results(turtle, turtletime, hare, haretime, timer);
    return (0);
}
void printInstructions(void)
{
    printf("Hello, Hello and welcome to all of the Annual 'Race to the Top' Challenge'! This is our xx year we at the 'Barnyard Society' have held this event and this year it looks to be a stormy one.\n");
    printf("Don't worry; our safety officals have inspected the spirla track, from the starting line at the base of Mt McDonald to the finish line at the very top, and deemed it safe enough to keep the races going. However, it is going to be poring alot so make sure to bundle up and have an umbrella out; if your racing today, be sure to have your personal protective equipment on, for it can get slippery along the trail and it's a 70 foot climb up the 5k steps worth of trails.");
    printf("Okay, lets get this party started");
    printf("\n");
    printf("\n");
    printf("\n");
    printf("And in the the next heat, two unlikely contestants in the running.\n");
    printf("\n");
    printf("In lane #1, we have....Mr. Turtle! He may seem slow and clumsy, but don't let that fool you for he can be quick on his toes when you least expect it. And can last longer in a sprint than anyone I have ever seen. Plus he is quite capable of adapting to wet terran, which means he has the home-court advantage today, given hwo rainy it is today.\n");
    printf("\n");
    printf("And in Lane #2, we have....Mr. Rabbit!. Oh he faster than lightning; I've seen it myself. Plus he's a pro on rough Terran. He currently holds several speed records on 'Short Distance Track'. Even so his greatest weaknest is his short stamina and weak traction on slippery ground, which is a handicap in today's weather. That could hurt him in this cross-country event.\n");
}
void moveTortoise(int *turtle)
{
    
}
void moveHare(int *hare)
{
    
}
void results(int turtle, int turtletime,  int hare, int haretime, int timer)
{
    printf("And the winner is...\n");
    printf("\n");
    printf("\n");
    if (turtletime < haretime)
        {printf("Mr. turtle!\n");
        printf("Congradulations Mr. Turtle, you did it in %d seconds. Looks like you'll have some leftovers after tonight's dinner.\n", turtletime);
        printf("Oh don't feel bad Mr. turtle. Your time of %d\n seconds is actually not that bad given the weather conditions outthere. Anyway, better luck next time.", turtletime);
        }
    if (turtletime > haretime)
        {printf("Mr. Rabbit!\n");
        printf("Congradulations Mr. Rabbit, you did it in %d seconds. Guess your belly is going to feel bloated tonight, will it?\n", haretime);
        printf("Oh don't feel bad Mr. Rabbitm. You've managed to do it in %d seconds. That's pretty good if you ask me, given the weather out here. Beside, there's always next year.\n", haretime);
        }
    else
        {printf("Oh wow, It's a tie!");
            printf("Unbelievable, they both did it in %d seconds.\n", timer);
            printf("Gues the two will be sharing the prize...unless of course the two are up for a rematch.\n");
        }
    printf("Anyway folks, lets give a round of applaus for both Mr. Turtle and Mr. Rabbit!\n");
    printf("\n");
    printf("Looks like the safety officals want to do a quick inspection of the trail. So were going to take a 5 minute break before the next heat. Stay warm and dry out there.\n");
}
