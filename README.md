#include <iostream>
using namespace std;

int mom;
int dad;


void Fullycb(){
cout << "This is your punnet square: " << endl;
cout << "     |    Xc    |     Xc    |     " << endl;
cout << "----------------------------------" << endl;
cout << "     |          |           |     " << endl;
cout << " Xc  |   XcXC   |   XcXc    |     " << endl;
cout << "     |          |           |     " << endl;
cout << "----------------------------------" << endl;
cout << "     |          |           |     " << endl;
cout << " Y   |   XcY    |   XcY     |     " << endl;
cout << "     |          |           |     " << endl;
cout << "----------------------------------" << endl;
cout << "     |          |           |     " << endl;
cout << "Males have a 100% of being colorblind" << endl;
cout << "females have a 100% of being colorblind" << endl;
cout << "females have a 0% of being silent carrier" << endl;

}
void Silentxnorm(){
cout << "This is your punnet square: " << endl;
cout << "     |    X     |     Xc    |     " << endl;
cout << "----------------------------------" << endl;
cout << "     |          |           |     " << endl;
cout << " X   |   XXc    |   XcX     |     " << endl;
cout << "     |          |           |     " << endl;
cout << "----------------------------------" << endl;
cout << "     |          |           |     " << endl;
cout << " Y   |   XY     |   XcY     |     " << endl;
cout << "     |          |           |     " << endl;
cout << "----------------------------------" << endl;
cout << "     |          |           |     " << endl;
cout << "Males have a 50% of being colorblind" << endl;
cout << "females have a 50% of being colorblind" << endl;
cout << "females have a 50% of being silent carrier" << endl;    
}

void norm(){
cout << "This is your punnet square: " << endl;
cout << "     |    X     |     X     |     " << endl;
cout << "----------------------------------" << endl;
cout << "     |          |           |     " << endl;
cout << " X   |   XX     |   XX      |     " << endl;
cout << "     |          |           |     " << endl;
cout << "----------------------------------" << endl;
cout << "     |          |           |     " << endl;
cout << " Y   |   XY     |   XY      |     " << endl;
cout << "     |          |           |     " << endl;
cout << "----------------------------------" << endl;
cout << "     |          |           |     " << endl;
cout << "Males have a 0% of being colorblind" << endl;
cout << "females have a 0% of being colorblind" << endl;
cout << "females have a 0% of being silent carrier" << endl;
}

void dadcb(){
cout << "This is your punnet square: " << endl;
cout << "     |    X     |     X     |     " << endl;
cout << "----------------------------------" << endl;
cout << "     |          |           |     " << endl;
cout << " Xc  |   XcX    |   XXc     |     " << endl;
cout << "     |          |           |     " << endl;
cout << "----------------------------------" << endl;
cout << "     |          |           |     " << endl;
cout << " Y   |   XY     |   XY      |     " << endl;
cout << "     |          |           |     " << endl;
cout << "----------------------------------" << endl;
cout << "     |          |           |     " << endl;
cout << "Males have a 0% of being colorblind" << endl;
cout << "females have a 50% of being colorblind" << endl;
cout << "females have a 50% of being silent carrier" << endl;
}

void momcb(){
cout << "This is your punnet square: " << endl;
cout << "     |    Xc    |     Xc    |     " << endl;
cout << "----------------------------------" << endl;
cout << "     |          |           |     " << endl;
cout << " X   |   XcX    |   XXc     |     " << endl;
cout << "     |          |           |     " << endl;
cout << "----------------------------------" << endl;
cout << "     |          |           |     " << endl;
cout << " Y   |   XcY    |   XcY     |     " << endl;
cout << "     |          |           |     " << endl;
cout << "----------------------------------" << endl;
cout << "     |          |           |     " << endl;
cout << "Males have a 100% of being colorblind" << endl;
cout << "females have a 50% of being colorblind" << endl;
cout << "females have a 50% of being silent carrier" << endl;
}

void silentxcb(){
cout << "This is your punnet square: " << endl;
cout << "     |    X     |     Xc    |     " << endl;
cout << "----------------------------------" << endl;
cout << "     |          |           |     " << endl;
cout << " Xc  |   XXc    |   XcXc    |     " << endl;
cout << "     |          |           |     " << endl;
cout << "----------------------------------" << endl;
cout << "     |          |           |     " << endl;
cout << " Y   |   XY     |   XcY     |     " << endl;
cout << "     |          |           |     " << endl;
cout << "----------------------------------" << endl;
cout << "     |          |           |     " << endl;
cout << "Males have a 50% of being colorblind" << endl;
cout << "females have a 75% of being colorblind" << endl;
cout << "females have a 25% of being silent carrier" << endl;
}

int main()
{
    
while(1==1){
    

    
cout << "-------Genetics Program-------" << endl;
cout << "Is your mother color blind" << endl;
cout << "1)if yes (2) if not: ";
cin >> mom;



while( mom < 1 || mom > 2 ){

cout << "Invalid input. Try again: ";
cin.clear(); // Reset input errors
cin.ignore(10000, '\n'); // Remove bad input
}

while (!(cin >> mom)) {  // Keep asking until the user enters a valid number
  cout << "Invalid input. Try again: ";
  cin.clear(); // Reset input errors
  cin.ignore(10000, '\n'); // Remove bad input
}


cout << "Is your father color blind" << endl;
cout << "1)if yes (2) if not: ";
cin >> dad;

while( dad < 1 || dad > 2 ){

cout << "Invalid input. Try again: ";
cin.clear(); // Reset input errors
cin.ignore(10000, '\n'); // Remove bad input
}

while (!(cin >> dad)) {  // Keep asking until the user enters a valid number
  cout << "Invalid input. Try again: ";
  cin.clear(); // Reset input errors
  cin.ignore(10000, '\n'); // Remove bad input
}


if(mom == 1 && dad == 1){
    
  Fullycb();
  
  
}

if(mom == 2 && dad == 1){
    
    dadcb();
    
    cout << "both of these could be your punnet square as you mom could be a silent carrier" << endl;
    
    silentxcb();
    
    
}

if(mom == 2 && dad == 2){
    
    norm();
    
    cout << "both of these could be your punnet square as you mom could be a silent carrier" << endl;
    
    Silentxnorm();
    
    
}

if(mom == 1 && dad == 2){
    
    momcb();
    
    
}


    
}


}
