#include <iostream> 
using namespace std;

int main(){ 
    
int guesscounter = 0;// the variable to count guesses    

srand(time(0));// to make sure a different number is generated each time the code id ran

int x = rand() % 101;// the random number variable 
int y;

do  {// runs the code first to check if the statement on line 45 is true before it loops (which it will)

guesscounter++;// to make the guesses count up and display automatically

cout << "Guess a Random number between 1-100: ";
cin >> y;

if (y == x){// states if the random number equals the number input it will display a win message 

cout << "you win the number was: " << x << endl;


} 

if (y < 1 || y > 100 ){
    
cout << "Invaild input try again";

return 0;
    
}

cout << "this is guess ." << guesscounter << endl;// displays the number of guesses
}
while (x >= 1 && x<= 100); //this loops the code with this statement that has to be true so the code would run in the first place


}

