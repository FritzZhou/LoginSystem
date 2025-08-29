// CREATE ANG LOGIN SYSTEM



#include <iostream>
using namespace std;

int main() {
    string name, pass;

    // Create initial account
    cout << "Create username: ";
    getline(cin, name);

    cout << "Create password: ";
    getline(cin, pass);

    while (true) {
        string cName, cPass;

        cout << "\n--- LOGIN ---\n";
        cout << "Enter username: ";
        getline(cin, cName);

        cout << "Enter password: ";
        getline(cin, cPass);

        if (cName == name && cPass == pass) {
            cout << "Hello, " << name << "! Login Successful.\n";
            break;
        } else {
            cout << "Login Failed!\n";
            cout << "Would you like to create a new account? (Y/N): ";
            string yn;
            getline(cin, yn);

            if (yn == "Y" || yn == "y") {
                cout << "Create username: ";
                getline(cin, name);

                cout << "Create password: ";
                getline(cin, pass);
            } 
            else if (yn == "N" || yn == "n") {
                cout << "Would you like to EXIT? (YES/NO): ";
                string exit;
                getline(cin, exit);

                if (exit == "YES" || exit == "yes") {
                    cout << "LOG OUT\n";
                    break;
                } else {
                    cout << "CONTINUE...\n";
                }
            } 
            else {
                cout << "Invalid choice. Exiting...\n";
                break;
            }
        }
    }

    return 0;
}
