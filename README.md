# Flavorful-Homework
This Repository contains some easy homework problems that I did some tinkering with. 

// 2. The Venti Café Mocha at Starbucks contains 410
// calories while the Grande size has 330 calories.
// If you have N (Number of drinks input by the user)
// Café Mocha’s per month how many calories will you save
// by switching from Venti to Grande? Your program should
// input the average number of drinks per month. Test your
// program with 10, 15 and 20 drinks per month.
//
// Samuel Sikes
// 1/22/15
// CS102 HMWK_2
// Problem #2
//
//
// This program asks if the user drinks Starbuck's Coffee. Then,
// it asks if the user drinks their Cafe Mochas. Next, it asks
// the user if they drink a Venti Cafe Mocha from Starbucks. After,
// the program offers the user an opportunity to get a tip. Finally,
// if the user specifies that they want a tip a printf() displays
// the difference, in calories, between a Venti and Grande Cafe Mocha.
// And supplies the user with the calorie savings they could receive,
// per month, if they switch from a Venti to a Grande Cafe Mocha. All the
// while, the program offers solutions to either a misstype or N(for no) to
// any of the questions asked to the user.
 
 
#include <stdio.h>
#include <stdlib.h>
#include <math.h>
#include <ctype.h>
 
#define CAL_ONE 330
#define CAL_TWO 410
 
int main(void)
{
     
    int num, calsaved;
    char answer0[10];
    char answer1[10];
    char answer2[10];
    char answer3[10];
     
     
    printf("\n\tDo you get coffee from Starbucks?");
    printf("\n\tPlease enter a Y or N (for yes or no): ");
    scanf(" %c", &answer0[1]); // asks user for y,Y,n,N
     
    if (toupper(answer0[1]) == 'N') // first if, runs if user enters: n, N
    {
        printf("\n\tWe can not all be fans of Starbucks.");
        printf("\n\tSorry, that you do not fancy their brew.");
    }
    else if (toupper(answer0[1]) == 'Y') // runs if user enters: y, Y
    {
        printf("\n\tDo you drink their Cafe Mocha's?");
        printf("\n\tPlease enter a Y or N (for yes or no): ");
        scanf(" %c",&answer1[1]); // asks user for y,Y,n,N
     
        if (toupper(answer1[1]) == 'Y') // second if, runs if user enters: y, Y
        {
            printf("\n\tGreat!\n\tDo you drink the Cafe Mocha in a Venti?");
            printf("\n\tPlease enter a Y or N (for yes or no): ");
            scanf(" %c",&answer2[1]); // asks user for y,Y,n,N
             
            if (toupper(answer2[1]) == 'Y') // third if, runs if user enters: y, Y
            {
                printf("\n\tWant a tip?");
                printf("\n\tEnter Y or N (for yes or no): ");
                scanf(" %c", &answer3[1]); // asks user for y,Y,n,N
                    if (toupper(answer3[1]) == 'Y') // fourth if, runs if user enters: y, Y
                    {
                        printf("\n\tA Venti Cafe Mocha from Starbucks has %d calories", CAL_TWO);
                                        // define function allows this constant (410) to be easily
                                        // re-defined at the top of the program
                        printf("\n\tand a Grande Cafe Mocha from Starbucks has %d calories.",
                               CAL_ONE); // define function allows this constant (330) to be easily
                                        // re-defined at the top of the program
                        printf("\n\tThe difference is 80 calories per coffee.");
                        printf("\n\tTo demonstrate the magnitude of change from a Venti to a");
                        printf("\n\tGrande sized Cafe Mocha, I would like you");
                        printf("\n\tto enter the number of Cafe Mocha's you drink");
                        printf("\n\tper month(enter as an integer(whole number)): ");
                         
                            scanf(" %d", &num); // asks user for integer
                 
                        calsaved = num * 80; // Number of calories saved per month
                     
                        printf("\n\tWow, that is %d Venti Cafe Mochas a month!", num);
                        printf("\n\tIf you choose to switch to Starbucks Grande Cafe Mochas,");
                        printf("\n\tyou could save a total of %d calories per month!!!", calsaved);
                    }
                    else if (toupper(answer3[1]) == 'N') // runs if user enters: n, N
                    {
                        printf("\n\tEnjoy your, 410 calorie, Venti Cafe Mocha without the tip!");
                        printf("\n\n\t:(");
                    }
                    else // if the user inputs anything other than y,Y,n,N this statement executes
                    {
                        printf("\n\tYou silly goose. You did not enter Y or N.");
                        printf("\n\tWell, at least you go to Starbucks.");
                        printf("\n\tBut, for the tip you will need to re-run");
                        printf("\n\tthe program.");
                        printf("\n\n\n\tps, IT IS A REALLY GOOD TIP");
                    }
                 
            }
            else if (toupper(answer2[1]) == 'N') // runs if user enters: n, N
            {
                printf("\n\tYou must be drinking a Cafe Mocha in a size");
                printf("\n\tother than Venti. Good job at being a responsible");
                printf("\n\tcoffee drinker!");
            }
            else // if the user inputs anything other than y,Y,n,N this statement executes
            {
                printf("\n\tYou silly goose. You did not enter Y or N.");
                printf("\n\tWell, at least you go to Starbucks");
                printf("\n\tand drink their Cafe Mochas.");
            }
        }
        else if(toupper(answer1[1]) == 'N') // runs if user enters: n, N
        {
            printf("\n\tToo bad!");
            printf("\n\tIt is a signature Starbuck's drink!");
        }
        else // if the user inputs anything other than y,Y,n,N this statement executes
        {
            printf("\n\tYou silly goose. You did not enter Y or N.");
            printf("\n\tWell, at least you go to Starbucks...");
        }
    }
    else // if the user inputs anything other than y,Y,n,N this statement executes
    {
        printf("\n\tYou silly goose. You did not enter Y or N.");
    }
     
     
     
     
     
    printf("\n\n");
    return 0;
     
     
} // End of main
