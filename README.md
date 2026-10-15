# Pps-project-smart-food-waste-alert-system

#include <stdio.h>

int main()
{
    float prepared, sold, leftover, waste;

    printf("Smart Food Waste Alert System\n");

    printf("Enter food prepared: ");
    scanf("%f", &prepared);

    printf("Enter food sold: ");
    scanf("%f", &sold);

    if (prepared <= 0 || sold < 0 || sold > prepared)
    {
        printf("Invalid quantity!\n");
        return 0;
    }

    leftover = prepared - sold;
    waste = (leftover / prepared) * 100;

    printf("Leftover food: %.2f\n", leftover);
    printf("Waste percentage: %.2f%%\n", waste);

    if (waste > 10)
        printf("Alert: High food waste!\n");
    else
        printf("Food waste is under control.\n");

    return 0;
}