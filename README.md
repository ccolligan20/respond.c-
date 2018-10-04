# respond.c-
#include <stdio.h>
#include <cs50.h>
#include <string.h>
#include <ctype.h>

string print_respond(string x);

int main()
{
    //ask user a question to declare variable
    printf("Do you want to go to the Cavs game? Enter (yes) or (no):\n");
    string i = get_string();
    //change yes or no to a capital Y or N
    i[0] = toupper(i[0]);
    printf("%s\n", i);
    //print outcome of respond function
    print_respond(i);
}

//create respond function
string print_respond(string i)
{
      //compare string (wether it is yes or no) and output response to type of string
      if (0 == strcmp(i, "Yes"))
        {
            printf("Okay I will get tickets!!\n");
        }
      if(0== strcmp(i, "No"))
        {
            printf("Okay then we will stay home...\n");
        }

        return i;
}
