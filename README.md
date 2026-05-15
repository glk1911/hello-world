this is like a calculator that also keeps inventory
#include <iostream>
#include <string>
#include <vector>
#include <iomanip>
using namespace std;

int componentnumj = 1;
float compwheight = 0;
float totalwheight;
string Componentname;
string Componenttype; 
float smallledav = 0.3;
float smallresav = 0.01;
float bigresav = 0.1;
float sevsegdis = 1.3;
float smallbutton = 1.9;
float smallswitch = 3.4;
vector<string> compnames; // Start with an empty list
string compname;
string cinv;
vector<int> compnums;
string location;
string compdem;
vector<string> compdemd;
vector<string> complocs;
int i = 0;

void Inventory(){

cout << "---------------------INVENTORY---------------------" << endl;
cout << "------|---name---|---stock---|-location-|--demand--|" << endl;


for (int i = 0; i < compnames.size(); i++) {
    cout << "item#" << left << setw(6) << i+1 << "|" << left << setw(10) << compnames[i] << "|" << left << setw(11) << compnums[i] << "|" << left << setw(10) << complocs[i] << "|" << left << setw(10) << compdemd[i] << "|" << endl;
}
        
}

void Inventorymode(){

do{
 
    
 
    cout << "Name your component: ";
    cin.ignore(1000, '\n');
    getline(cin, compname);

    compnames.push_back(compname);
    
    cout << "how much does one " << compnames[i] << " wheigh(g): ";
    while (!(cin >> compwheight)) {  // Keep asking until the user enters a valid number
  cout << "Invalid input. Try again: ";
  cin.clear(); // Reset input errors
  cin.ignore(10000, '\n'); // Remove bad input
}
    
    cout << "how much does all " << compnames[i] << " wheigh(g): ";
    while (!(cin >> totalwheight)) {  // Keep asking until the user enters a valid number
  cout << "Invalid input. Try again: ";
  cin.clear(); // Reset input errors
  cin.ignore(10000, '\n'); // Remove bad input
}
    
    float componentnum = totalwheight / compwheight;
    cout << "The total number of " << compnames[i] << " is: " << (int)componentnum << endl;
    
    compnums.push_back(componentnum);
    
    cout << "where is your component located in the shop: ";
    cin.ignore(1000, '\n');
    getline(cin,location);
    
    complocs.push_back(location);
    
    cout << "Is this item in demand in the shop (y for yes n for no): "; 
    cin >> compdem;
    
    if(compdem == "y"){
        compdemd.push_back("Restock");
    }
    
    if(compdem == "n"){
        compdemd.push_back("Stable");
    } 
    while(compdem != "n" && compdem != "y"){
    cout << "Invalid input try again: ";
    }
    
    cout << "your item is complete and has been added to the Inventory," <<
    "\n Would you like to see your Inventory(y for yes n for no) or press e to end the program";
    cin >> cinv;  
    
    if(cinv == "y"){
     Inventory();
    }
    
    if(cinv == "n"){
        
    } 
    
    if(cinv == "e"){
        return;
    }
    
    while(cinv != "n" && cinv != "y" && cinv != "e"){
    cout << "Invalid input try again: ";
    }
    
    i++;
    
    }while(i > 0);


}



int main() {
string mode;
cout << "***************************************" << endl;
cout << "------------Welcome to SECC------------" << endl;
cout << "(Small Electrical Component Calculator)" << endl;
cout << "-------& Inventory keeping system------" << endl;
cout << "***************************************" << endl;
cout << "this system uses weight to calculate components" << endl;
cout << "pick your mode 1) for short term, 2) for inventory mode: ";
cin >> mode;

if(mode == "1"){
    
}

if(mode == "2"){
    Inventorymode();
}

while(mode != "2" && mode != "1" ){
    cout << "Invalid Input. Try again: ";
}


while (true) {
cout << "Enter the Component type of Component#" << componentnumj 
<< ", 1)small resistor, 2)big resistor, 3)small led, 4)7 segment display, 5)small button, 6)small switch"
<< " Or press e to end: ";
 
cin >> Componenttype;


if (Componenttype == "e") {
return 0;
}


while (Componenttype != "1" && Componenttype != "2" && Componenttype != "3" &&
Componenttype != "4" && Componenttype != "5" && Componenttype != "6") {
cout << "Invalid Input. Try again: ";
cin >> Componenttype;
if (Componenttype == "e") return 0;
}

if (Componenttype == "1") compwheight = smallresav;
else if (Componenttype == "2") compwheight = bigresav;
else if (Componenttype == "3") compwheight = smallledav;
else if (Componenttype == "4") compwheight = sevsegdis;
else if (Componenttype == "5") compwheight = smallbutton;
else if (Componenttype == "6") compwheight = smallswitch;

cin.ignore(1000, '\n');


cout << "Name your Component: ";
getline(cin, Componentname);

cout << "Please Weigh component(s)" << Componentname << " in (g): ";
cin >> totalwheight;

float componentnum = totalwheight / compwheight;
cout << "The total number of " << Componentname << " is: " << (int)componentnum << endl;
   
componentnumj++; 
    }
    

}

