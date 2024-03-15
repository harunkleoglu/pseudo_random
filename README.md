
# Pseudo Random Number Generator

This simple C/C++ header file generates random numbers using the [linear congruential method](https://en.wikipedia.org/wiki/Linear_congruential_generator). It also includes a function to set the initial seed based on the number of CPU cycles.

## Usage

Include the header file in your project and call the `rand()` or `rand_range(min, max)` functions to use random numbers.

```c
#include "pseudo_random.h"
#include <stdio.h>

int main() {
    // Set the seed to generate random numbers
    srand(123); // Example seed

    // Example: Generate a random number between 1 and 10
    int random_number = rand_range(1, 10);
    printf("Random number: %d\n", random_number);

    return 0;
}
```
## Functions

Include the header file in your project and call the `rand()` or `rand_range(min, max)` functions to use random numbers.

-   `void srand(unsigned int c_seed)`: Used to set the seed of the random number generator.
-   `int rand()`: Returns a random integer.
-   `int rand_range(int min, int max)`: Returns a random integer within a specific range (including min and max).
-   `void random_seed_by_cpu_cycle()`: Sets a random seed based on the number of CPU cycles.

## Note

This random number generator is suitable for simple applications but is not appropriate for security or cryptographic applications. More secure random number generators should be preferred.
