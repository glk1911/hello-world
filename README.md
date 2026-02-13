#include <iostream>
using namespace std; // makes it so I don't have to do std:: for everything

int main(){
int x;  

cout << "Enter your Miles driven: "; // ask for miles driven so it can de diveded
cin >> x;

int y;

cout << "Enter the amount of used gas (g): "; // ask for the amount of gas used in gallons so it can be input into the mpg formula
cin >> y;

int z = x/y; // the miles per gallon formula

cout << "Your Miles Per Gallon is: " << z << endl; // displays the mpg 

}
