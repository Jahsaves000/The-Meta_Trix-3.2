# The-Meta_Trix-3.2
CS50 lecture 2 (Arrays)

#include <cs50.h>
#include <stdio.h>

int main(void)
{
    string name = get_string("When's your birthday?\n ");
    printf("Happy birthday! ");
}



//new code
#include <stdio.h>

int main(void)
{
    int score1 = 72;
    int score2 = 73;
    int score3 = 33;

    printf("Average: %f\n", (score1 + score2 + score3) / 3.0);
}

/final outcome of that ^ code

(new corrected version)
#include <stdio.h>
#include <cs50.h>

float average(int length, int array[]);
const int TOTAL = 3;

int main(void)
{
    int scores[TOTAL];
    for (int i = 0; i < 3; i++)
    {
    scores[i] = get_double("Score: ");
    }

    printf("average: %f\n", average(TOTAL, scores));
}

float average(int length, int array[])
{
    float sum = 0.0;
    for (int i = 0; i < length; i++)
    {
        sum += array[i];
    }
    return sum / (float) length;
}


include <stdio.h>

int main(void)
{
    char c = '#';
    
    printf("%c\n", c);
}


//string.c
(new code)

#include <cs50.h>
#include <stdio.h>
#include <string.h>

int main(void)
{
    string s = get_string("Input: ");
    printf("Output: ");
    
    for (int i = 0, n = strlen(s); i < n; i++)
    {
        printf("%c", s[i]);
    }
    printf("\n");
}


/*uppercase.c
(new code)

#include <cs50.h>
#include <stdio.h>
#include <string.h>

int main(void)
{
    string s = get_string("Before: ");
    printf("After: ");
    
    for (int i = 0, n = strlen(s); i < n; i++)
    {
        if (s[i] >= 'a' && s[i] <= 'z')
        {
            printf("%c", s[i] ???)
        }
        else
        {
            printf("%c", s[i])
        }
    }
    printf("\n");
}



