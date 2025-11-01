#include <stdio.h> 
#include <stdlib.h>
#include <time.h>
 
int main(){
 int random,guess;
 int no_of_guess = 0;
 srand(time(NULL));

 printf(" Welcome to the world of guessing Numbers\n ");
 random = rand() * 100 + 1; //genrating between 0 to 100

 do{
     printf(" \n Please enter your guess between(1 to 100): ");
     scanf("%d",&guess);
     no_of_guess++;
 
     if (guess < random) {
      printf("Guess a larger number. \n");
     } else if (guess > random) {
     printf("Guess a smaller number. \n");
     }else {
        printf("Congratulations !!You have successfully guess the Numberin %d attempts", no_of_guess);
     }

    }while (guess !=random);

     printf(" \n Bye bye, Thanks for Playing.");
     printf("\nDevloped by: Sushil Kumar");
     return 0;
                                       
}                        
