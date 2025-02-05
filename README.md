# include <stdio.h>
#include <stdlib.h>
# include <time.h>
int main()
{
    int number, guess, attempts = 0;
    srand(time(0));//srand - standard random
    number = rand() % 100 +1;
    printf("Welcome to the number guessing game!:\n");
    printf("I have selected a number betwwen 1 and 100. Can you guess what it is?\n");
    do{
        printf("Enter your guess: ");
        scanf("%d", &guess);
        attempts++;
        if(guess < number){
            printf("Too low! Try again. \n");
        }
        else if(guess > number){
            printf("Too high! Try again.\n");
        }
        else{
            printf("Congragulations! you guesed the number in %d attempts.\n", attempts);
        }
        
    }while(guess != number);
        return 0;
}
