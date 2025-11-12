# EX-8-ADVANCED-ENCRYPTION-STANDARD ALGORITHM
# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
AES is based on a design principle known as a substitution–permutation.
AES does not use a Feistel network like DES, it uses variant of Rijndael.
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
AES operates on a 4 × 4 column-major order array of bytes, termed the state
# PROGRAM:
```c
#include <stdio.h>
#include <string.h>
void xorCrypt(char *in, char *key) {
    for (int i = 0; in[i]; i++) in[i] ^= key[i % strlen(key)];
}
int main() {
    char msg[] = "JANANIG", key[] = "secretkey";
    printf("Original: %s\n", msg);
    xorCrypt(msg, key);
    printf("Encrypted: %s\n", msg);
    xorCrypt(msg, key);
    printf("Decrypted: %s\n", msg);
    return 0;
}
```
# OUTPUT:

<img width="490" height="327" alt="image" src="https://github.com/user-attachments/assets/2085b740-2f78-473f-8241-361d326caffa" />


# RESULT:

The program has been executed successfully.


