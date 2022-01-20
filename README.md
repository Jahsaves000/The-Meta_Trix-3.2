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

/*another variation
/*another variation
<<<<<<< branch-0.0
(same code ^)

#include <cs50.h>
#include <ctype.h>
#include <stdio.h>
#include <string.h>

int main(void)
{
    string s = get_string("Before: ");
    printf("After: ");
    
    for (int i = 0, n = strlen(s); i < n; i++)
    {
        if (islower(s[i]))
        {
            printf("%c", toupper(s[i]));
        }
        else
        {
            printf("%c", s[i]);
        }
    }
    printf("\n");
}

/*and another one
()

#include <cs50.h>
#include <ctype.h>
#include <stdio.h>
#include <string.h>

int main(void)
{
    string s = get_string("Before: ");
    printf("After: ");
    
    for (int i = 0, n = strlen(s); i < n; i++)
    {
       printf("%c", toupper(s[i]));
    }
    printf("\n");
}


/*next code*/

The first line tells us that our function "main" will take one integer(number) as an input and an array ([]) of strings as input. Argc is shorthand notation for argument count and argument count is an integer tha's going to represent the number of words hat  the user tyes at the prompt. Argv is short for argument vector. A vector is a list. It is  a variable that going to store all of the strings in an array that a human types after our program's name. So, this first line reads that if the person types two words in at the prompt, then I'll say "hello, name". If not the I'll just print hello, world. So what the computer does is it's going to store in argc a number of the total words that the person typed in, not just the the arguments, tecnically all of the words includin our own program's name. Its then going to fill the array of strings(argv) with all of the words the human typed at the prompt, so not just the arguments like Brian or David, but also the name of your program. So, if the human typed in twon total ewords like (argv) Brian, then i want to pring out hello followed by a placeholder and then whatever value is at argv[1]. So the reason we use 1 instead of 0 is because argv is an array and the array name is stored at the zeroeth place in this array.


#include <cs50.h>
#include <stdio.h>

int main(int argc, string argv[])
{
    if (argc == 2)
    {
        printf("hello, %s\n", argv[1]);
    }
    else
    {
        printf("hello, world\n");
    }
}
