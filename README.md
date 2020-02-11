# Simple-Calculator-
basic calc in c++
#include <iostream>
#include <stdlib.h>

using namespace std;

void simpleCal(){
    cout << "\n\n\n **************************************** \n\n" << endl;
    cout << "      THIS IS A DOPE CALCULATOR \n\n" << endl;
    cout << " **************************************** \n\n" << endl;
}

int getUserInput(){
   int num1;
   char op;
   int num2;

   cout << " \t Please input a number" << endl;
   cin >> num1;
   cout << " \t Input operator" << endl;
   cin >> op;
   cout << " \t Please input a second number" << endl;
   cin >> num2;

   if (op == '+'){
        cout << "The Sum of " << num1 <<" & " << num2 << " is " << num1 + num2 << "\n\n";
        return num1 + num2;
    }
    else if (op == '-'){
        cout << "The difference of " << num1 <<" & " << num2 << " is " << num1 - num2 << "\n\n";
        return num1 - num2;
    }
    else if (op == '*'){
        cout << "The product of " << num1 <<" & " << num2 << " is " << num1 * num2 << "\n\n";
        return num1 * num2;
    }
    else if (op == '/'){
        cout << "The result of " << num1 <<" divided by " << num2 << " is " << num1 / num2 << "\n\n";
        return num1 / num2;
    }
    else {
        system ("CLS");
        cout << "Invalid operator! Pleas try again \n" << flush;
        system ("PAUSE");
        system ("CLS");
        simpleCal();
        getUserInput();
    }
}


int main(){
    simpleCal();
    getUserInput();

    char userResponse;
    cout << " Would you like to continue using the calculator? y/n: ";
    cin >> userResponse;

    if (userResponse == 'y'){
        system ("CLS");
        cout << "WELCOME BACK \n" << flush;
        system ("PAUSE");
        system ("CLS");
        simpleCal();
        getUserInput();
    }
    else {
        system("CLS");
        cout << " Goodbye..... \n" << flush;
        system("EXIT");
    }

return 0;
}
