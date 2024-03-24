# rock-paper-scissors-game

#include<stdio.h>
#include<stdlib.h>
#include<time.h>

int rockpaperscissors( char you, char comp){
// Condition for draw
if(you == comp){
return 0;
}

// Non draw conditions 
if(you == 'r' && comp == 's'){
return 1;
}

if(you == 's' && comp == 'r'){
return -1;
}

if(you== 'r' && comp == 'p'){
return 1;
}

if(you== 'p'&& comp== 'r'){
return -1;
}

if(you== 's' && comp == 'p'){
return 1;
}

if(you== 'p'&& comp == 's'){
return -1;
}

}

int main(){
char you, comp;

srand(time(0)); //To chose random rock, paper and scissors 

int number=rand()%100+1; //To select random possibility from 1 to 100 to select rock, paper scissors 
 
 if (number <= 33){
  comp='r';
 }
else if(number >33 && number <=66){
  comp='p';
 }
 
 else{
  comp='s';
 }
 
 printf("Enter 'r' for rock, 'p'for paper and 's' for scissors: ");
 scanf("%c" ,&you);
 
 int result = rockpaperscissors( you, comp);
 

 printf("You chose %c and computer chose %c\n",you,comp);
 if(result==0){
 printf("Game Draw!!!");
 }
 
else if(result==1){
 printf("You Win!!!");
 }
 
 else{
 printf("You Lose!!!");
 }
 
 return 0;
}
