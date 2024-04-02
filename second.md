On a specific day, the exchange rates were as follows: the British pound was valued at $1.487 U.S., the French franc at $0.172, the German deutschemark at $0.584, and the Japanese yen at $0.00955. Write a program that prompts the user to input an amount in U.S. dollars. The program should then display this amount converted into these four other currencies. Test the program by inputting various dollar amounts and ensuring that the conversions to British pounds, French francs, German deutschemarks, and Japanese yen are accurate. Additionally, test the program with negative dollar amounts to verify that it handles invalid input appropriately.

#include <iostream>
using namespace std;
int main() {
    double exchangeRates[4] = {1.487, 0.172, 0.584, 0.00955};
    double dollars;
    cout << "Enter an amount in US dollars: ";
    cin >> dollars;
    if(dollars < 0) {
        cout << "Invalid input! Please enter a positive value.\n";
        return 1;
    }
    cout << "\nExchange Rates:\n";
    cout << "British Pound: $" << exchangeRates[0] << "\n";
    cout << "French Franc: $" << exchangeRates[1] << "\n";
    cout << "German Deutschemark: $" << exchangeRates[2] << "\n";
    cout << "Japanese Yen: $" << exchangeRates[3] << "\n";
    cout << "\nConverted Values:\n";
    cout << "British Pound: $" << dollars * exchangeRates[0] << "\n";
    cout << "French Franc: $" << dollars * exchangeRates[1] << "\n";
    cout << "German Deutschemark: $" << dollars * exchangeRates[2] << "\n";
    cout << "Japanese Yen: $" << dollars * exchangeRates[3] << "\n";
    cout<<"Program is created by Tarun"<<endl;
    cout<<"rollnumber:2310997308"<<endl;
    return 0;
}
