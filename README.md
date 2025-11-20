#include <stdio.h>

int main() {
    int choice;
    float num1, num2;

    // Displaying Menu
    printf("===== SIMPLE CALCULATOR =====\n");
    printf("1. Addition\n");
    printf("2. Subtraction\n");
    printf("3. Multiplication\n");
    printf("4. Division\n");
    printf("5. Modulus\n");
    printf("=============================\n");
    printf("Enter your choice (1-5): ");
    scanf("%d", &choice);

    // Taking Inputs
    printf("Enter first number: ");
    scanf("%f", &num1);

    printf("Enter second number: ");
    scanf("%f", &num2);

    // Performing Operations
    switch(choice) {
        case 1:
            printf("Result: %.2f\n", num1 + num2);
            break;

        case 2:
            printf("Result: %.2f\n", num1 - num2);
            break;

        case 3:
            printf("Result: %.2f\n", num1 * num2);
            break;

        case 4:
            if(num2 == 0)
                printf("Error! Division by zero is not allowed.\n");
            else
                printf("Result: %.2f\n", num1 / num2);
            break;

        case 5:
            printf("Result: %d\n", (int)num1 % (int)num2);
            break;

        default:
            printf("Invalid Choice!\n");
    }

    return 0;
}
