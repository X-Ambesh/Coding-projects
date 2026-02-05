#To check if the credit card number is valid or not 

    #include <iostream>
    using namespace std;
    int evenDigits(string creditCardNumber);
    int oddDigits(string creditCardNumber);
    int main()
    {
        string creditCardNumber;
        cout << "Enter your credit card number: ";
        cin >> creditCardNumber;
        int totalSum = evenDigits(creditCardNumber) +   oddDigits(creditCardNumber);
        if (totalSum % 10 == 0)
            cout << "The credit card number is valid."  << endl;
        else
            cout << "The credit card number is invalid."    << endl;
    }
    int evenDigits(string creditCardNumber)
    {
        int sumEven = 0;
        for (int i = creditCardNumber.length() - 2; i >=    0; i -= 2)
        {
            int digit = (creditCardNumber[i] - '0') * 2;
            if (digit > 9)
                digit -= 9;
            sumEven += digit;
        }
        return sumEven;
    }
    int oddDigits(string creditCardNumber)
    {
        int sumOdd = 0;
        for (int i = creditCardNumber.length() - 1; i >=    0; i -= 2)
        {
            sumOdd += (creditCardNumber[i] - '0');
        }
        return sumOdd;
    }
#Sample run

    Enter your credit card number:  4587090079089045                               
    The credit card number is valid.       
