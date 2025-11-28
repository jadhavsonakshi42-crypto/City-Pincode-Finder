#include <stdio.h>

int main() {
    int pin[6] = {110001, 400001, 560001, 700001, 600001, 380001};
    char city[6][20] = {
        "New Delhi", "Mumbai", "Bangalore",
        "Kolkata", "Chennai", "Ahmedabad"
    };

    int input, found = 0;

    printf("Enter PIN code: ");
    if (scanf("%d", &input) != 1) {
        printf("Invalid input! Please enter numeric PIN code.\n");
        return 0;
    }

    for (int i = 0; i < 6; i++) {
        if (pin[i] == input) {
            printf("City: %s\n", city[i]);
            found = 1;
            break;
        }
    }

    if (!found)
        printf("PIN Code Not Found.\n");

    return 0;
}
