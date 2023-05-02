#include <stdio.h>

// Function to find the sum of digits of a number
int sumOfDigits(int n) {
    int sum = 0;
    while(n > 0) {
        sum += n % 10;
        n /= 10;
    }
    return sum;
}

int main() {
    int sum = 0;
    // Loop to find all even 4-digit numbers
    for(int i = 1000; i <= 9998; i += 2) {
        sum += i;
    }
    // Loop to keep adding digits until a single digit is found
    while(sum > 9) {
        sum = sumOfDigits(sum);
    }
    // Checking if the single digit is odd or even
    if(sum % 2 == 0) {
        printf("Even found\n");
    }
    else {
        printf("Odd found\n");
    }
    return 0;
}
