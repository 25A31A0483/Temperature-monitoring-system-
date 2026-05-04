# Temperature-monitoring-system-
Temperature monitoring system 
#include <stdio.h>

int main() {
    float temperature;
    int choice;

    while (1) {
        printf("\n--- Temperature Monitoring System ---\n");
        printf("Enter temperature in Celsius: ");
        scanf("%f", &temperature);

        if (temperature < 0) {
            printf("Status: Freezing ❄️\n");
        } 
        else if (temperature >= 0 && temperature <= 35) {
            printf("Status: Normal 😊\n");
        } 
        else if (temperature > 35 && temperature <= 45) {
            printf("Status: High ⚠️\n");
        } 
        else {
            printf("Status: Critical 🔥\n");
        }

        printf("\nDo you want to continue? (1 = Yes / 0 = No): ");
        scanf("%d", &choice);

        if (choice == 0) {
            printf("Exiting program...\n");
            break;
        }
    }

    return 0;
}
