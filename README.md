#include <iostream>
Using namespace std;

int main(){
double x;  

cout << "Enter your 1st MPG value (g): ";
cin >> x;

double y;

cout << "Enter your 2nd MPG value (g): ";
cin >> y;

double z = (x + y)/2;

cout << "Your Average MPG is: " << z << endl;

double r;

cout << "what is the maximum amount of gas your car can hold (g): ";
cin >> r;

double v = r*z;

cout << "your Distance per tank of gas is: " << v << endl;


}

