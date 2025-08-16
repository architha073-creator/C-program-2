# C-program-2
Atm limited
#include <stdio.h>
int main()
{
    int amnt, c100, c50, c10;
    printf("Enter total amount: ");
    scanf("%d", &amnt);
    printf("Enter available Rs 100 notes: ");
    scanf("%d", &c100);
    printf("Enter available Rs 50 notes: ");
    scanf("%d", &c50);
    printf("Enter available Rs 10 notes: ");
    scanf("%d", &c10);

    int n100=0, n50=0, n10=0; // notes actually used

    // Allocate Rs 100 notes
    n100 = amnt / 100;
    if (n100 > c100)
        n100 = c100;
    amnt -= n100 * 100;

    // Allocate Rs 50 notes
    n50 = amnt / 50;
    if (n50 > c50)
        n50 = c50;
    amnt -= n50 * 50;

    // Allocate Rs 10 notes
    n10 = amnt / 10;
    if (n10 > c10)
        n10 = c10;
    amnt -= n10 * 10;

    printf("Number of Rs 100 notes used: %d\n", n100);
    printf("Number of Rs 50 notes used : %d\n", n50);
    printf("Number of Rs 10 notes used : %d\n", n10);
    printf("Remaining amount not dispensable: %d\n", amnt);

    return 0;
}
