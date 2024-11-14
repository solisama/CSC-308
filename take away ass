#include <stdio.h>
#include <stdlib.h>
#include <ctype.h>

int main() {
    char input[50];
    printf("Enter a character, integer, or float: ");
    fgets(input, sizeof(input), stdin); // using fgets for safer input

    // Remove newline character if present from input
    input[strcspn(input, "\n")] = 0;

    // Switch to check type based on the first character or format of input
    switch (1) {
        // Check if the input is a character
        case 1:
            if (isalpha(input[0])) {
                char ch = input[0];
                printf("\nInput type: Character\n");
                printf("ASCII Value: %d\n", ch);
                printf("Size of Character: %lu bytes\n", sizeof(ch));
                printf("Next 4 characters (increments of 3):\n");
                for (int i = 1; i <= 4; i++) {
                    char nextChar = ch + (i * 3);
                    printf("%c (ASCII: %d)\n", nextChar, nextChar);
                }
                break;
            }

        // Check if the input is a float
        case 2:
            if (strchr(input, '.')) {
                float num;
                sscanf(input, "%f", &num);
                printf("\nInput type: Float\n");
                printf("Size of Float: %lu bytes\n", sizeof(num));
                printf("Next 4 floats (increments of 3.0):\n");
                for (int i = 1; i <= 4; i++) {
                    float nextFloat = num + (i * 3.0f);
                    printf("%.2f\n", nextFloat);
                }
                break;
            }

        // Check if the input is an integer
        case 3:
            if (isdigit(input[0]) || (input[0] == '-' && isdigit(input[1]))) {
                int num;
                sscanf(input, "%d", &num);
                printf("\nInput type: Integer\n");
                printf("Size of Integer: %lu bytes\n", sizeof(num));
                printf("Next 4 integers (increments of 3):\n");
                for (int i = 1; i <= 4; i++) {
                    int nextInt = num + (i * 3);
                    printf("%d\n", nextInt);
                }
                break;
            }

        // Default case if input type cannot be identified
        default:
            printf("Error: Invalid input.\n");
    }

    return 0;
}
