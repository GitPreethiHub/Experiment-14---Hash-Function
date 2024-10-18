# Experiment-14---Hash-Function
## Aim
To implement a cryptographic hash function to compute the hash of a message.

## Algorithm Steps:

1) Choose a cryptographic hash function (e.g., SHA-256).
2) Input a message and apply the hash function.
3) Compute the hash value.
4) Output the fixed-size hash value.
5) Hashing is a one-way process and does not involve encryption or decryption.

## Program
```
#include <stdio.h>
#include <string.h>

unsigned long simple_hash(char *str) {
    unsigned long hash = 5381;
    int c;
    while ((c = *str++)) {
        hash = ((hash << 5) + hash) + c;
    }
    return hash;
}

int main() {
    printf("Experiment 14 - Hash Function\n");
    printf("Developed by: Preethi M 212222100037\n");

    char message[] = "preethi";
    unsigned long hash = simple_hash(message);

    printf("Message: %s\n", message);
    printf("Hash: %lu\n", hash);

    return 0;
}

```
## Output
![image](https://github.com/user-attachments/assets/74d8c3b9-0a17-4004-b807-850f3decd6c4)

## Result
The hash value of the message is successfully computed using a simple hash function.
