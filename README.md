#include <stdio.h>

int main() {
    char businessName[50];
    float sales, expenses, profit;

    printf("========================================\n");
    printf("       BUSINESS MANAGEMENT SYSTEM\n");
    printf("========================================\n");

    printf("Enter business name: ");
    scanf(" %[^\n]", businessName);

    printf("Enter total sales ($): ");
    scanf("%f", &sales);

    printf("Enter total expenses ($): ");
    scanf("%f", &expenses);

    profit = sales - expenses;

    printf("\n========================================\n");
    printf("           BUSINESS REPORT\n");
    printf("========================================\n");

    printf("Business Name : %s\n", businessName);
    printf("Total Sales   : $%.2f\n", sales);
    printf("Expenses      : $%.2f\n", expenses);

    if (profit > 0) {
        printf("Profit        : $%.2f\n", profit);
        printf("Status        : PROFIT\n");
    }
    else if (profit < 0) {
        printf("Loss          : $%.2f\n", -profit);
        printf("Status        : LOSS\n");
    }
    else {
        printf("Profit/Loss   : $0.00\n");
        printf("Status        : NO PROFIT / NO LOSS\n");
    }

    printf("========================================\n");

    return 0;
}
