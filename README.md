#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int dice;
    char choice;

    srand(time(0));

    printf("🎲 LUDO DICE ANALYZER 🎲\n");

    do {
        dice = (rand() % 6) + 1;
        printf("\nYou rolled: %d\n", dice);

        if (dice == 6)
            printf("Great! You got a SIX. You get another chance!\n");
        else if (dice == 1)
            printf("Oops! Just a ONE. Better luck next roll.\n");
        else
            printf("Nice roll!\n");

        printf("\nDo you want to roll again? (y/n): ");
        scanf(" %c", &choice);

    } while (choice == 'y' || choice == 'Y');

    printf("\nThanks for playing Ludo Dice Analyzer!\n");
    return 0;
}
