#include <iostream>
using namespace std;


int main()
{
 
//monthly expenses
   
double monthlypayment;
double insurance;
float fulltank;
float weeklygas;
float percent = 100; // used to give a number as a percent
int interest; 
float Irate = interest / percent;
float adtexp;

 
 //annual expenses
 
 cout << "How much is your monthly car loan: "; // first requirement
 cin >> monthlypayment;

 cout << "how much is your mandatory liability insurance per month: ";
 cin >> insurance;

 cout << "how much does a full tank of gas cost: "; // looking to get a more precise calculation of the users monthly gas expenses by splitting it up into parts then using an equation to add them together
 cin >> fulltank;

 cout << "How many times do fill your gas per week: "; // the second part of the equation that will be multiplied by four
 cin >> weeklygas;

 float monthlygasprice = fulltank * weeklygas * 4; // equation stored in one variable

 cout << "This is your monthly gas price: " << monthlygasprice << endl; // displays the result of the equation stored in monthlygasprice 

 cout << "what is your monthly interest rate on your monthly payment(no %): "; // using this to accurately find the true annual cost of their automobile. Telling the user no to input the % as it means something else in c++
 cin >> interest;
 
 cout << " what is cost of any addtional and consistant expenses(if none skip by entering zero): "; // tires, maintinance, and oil aren't consistent expenses so i added this just in cases someone has a routine change of one of these things or something else similar
 cin >> adtexp;
 
 float tmc = monthlypayment + monthlypayment * Irate + monthlygasprice + adtexp + insurance;
 
 cout << "the total monthly cost of your vehicle(assuming its not your first month) is: $" << tmc << endl; // total monthly cost display
}
