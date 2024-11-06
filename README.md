
# series
#include <stdio.h>
#include <stdbool.h>
#include <math.h>

// Function declarations
void fibonacci(int limit);
void prime(int limit);
void xPowerX(int limit);

int main() {
    int choice, limit;

    // Display options for series
    printf("Choose a series to generate:\n");
    printf("1. Fibonacci Series\n");
    printf("2. Prime Numbers\n");
    printf("3. X^X Series\n");
    printf("Enter your choice (1-3): ");
    scanf("%d", &choice);

    // Ask user for limit
    printf("Enter the limit for the series: ");
    scanf("%d", &limit);

    // Call the appropriate function based on choice
    switch(choice) {
        case 1:
            fibonacci(limit);
            break;
        case 2:
            prime(limit);
            break;
        case 3:
            xPowerX(limit);
            break;
        default:
            printf("Invalid choice!\n");
    }

    return 0;
}
void fibonacci(int limit) {
    int a = 0, b = 1, next;
    printf("Fibonacci Series up to %d:\n", limit);

    for (int i = 1; i <= limit; i++) {
        printf("%d ", a);
        next = a + b;
        a = b;
        b = next;
    }
    printf("\n");
    }
void prime(int limit) {
    printf("Prime Numbers up to %d:\n", limit);
    for (int num = 2; num <= limit; num++) {
        bool isPrime = true;
        for (int i = 2; i <= sqrt(num); i++) {
            if (num % i == 0) {
                isPrime = false;
                break;
            }
        }
        if (isPrime) {
            printf("%d ", num);
        }
    }
    printf("\n");
}

void xPowerX(int limit) {
    printf("X^X Series up to %d:\n", limit);
    for (int i = 1; i <= limit; i++) {
        printf("%.0f ", pow(i, i));
