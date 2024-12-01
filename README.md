# C-programming-

#include <stdlib.h>
#include <stdio.h>
#include <time.h>

int main(void) {
    // Put the seed
    srand((unsigned int)time(0));
    
    // Generating a random number within the range 1 to 100
    int range_of_numbers = (rand() % 100) + 1;
    int number_guess = 0;
    int guessed = 0;

    do {
        printf("The guess no:\n");
        scanf("%d", &guessed);  // Update guessed here

        if (guessed > range_of_numbers) {
            printf("Go lower!\n");
        } else if (guessed < range_of_numbers) {
            printf("Go higher!\n");
        } else {
            printf("Congrats!\n");
        }

        number_guess++;  // Increment guess counter
    } while (guessed != range_of_numbers);  // Loop until guessed number matches

    printf("The number of guesses is %d\n", number_guess);
    return 0;
}
