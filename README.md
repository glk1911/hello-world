#include <iostream>
Using namespace std; // makes it so I don't have to do std:: for everything

int main(){
double x;  // I'm using double so the user can input decimals

cout << "Enter your 1st MPG value (g): "; // ask you for the a value to get the average
cin >> x;

double y;

cout << "Enter your 2nd MPG value (g): ";
cin >> y;

double z = (x + y)/2; // the average miles per gallon formula

cout << "Your Average MPG is: " << z << endl; //the average miles per gallon

double r;

cout << "what is the maximum amount of gas your car can hold (g): ";
cin >> r;

double v = r*z; // the distance per tank of gas formula

cout << "your Distance per tank of gas is: " << v << endl; // the final answer


}

