# Lecture-15-Functions

Lecture 15 Functions Part 1

SLIDE 11, Declaring and Defining

    #include <iostream>
    using namespace std; 

    void welcome(); //function declaration

    int main() {
        welcome(); //function call
        return 0;
    }

    void welcome() { //function definition

        cout << "Welcome to BSU" << endl;
    }
    
SLIDE 12, You say hello, I say goodbye

    #include <iostream>
    using namespace std;

    void first() {
        cout << "Welcome" << endl;
    }

    void second() {
        cout << "End of program" << endl;
    }

    int main()
    {
        first();
        second();
    }

Lecture 15 

EXERCISE BREAK

SLIDE 8, Time

    #include <iostream>
    using namespace std;

    /*return type set to string as this function will return a string value back to main program*/

    string greetings(int time)
    {
        //evaluate int value passed in and set return message
        if (0 >= time || time <= 11)
        {
            return "\nGood Morning";
        }
        else if (12 >= time || time <= 17)
        {
            return "\nGood Afternoon";
        }
        else if (18 >= time || time <= 21)
        {
            return "\nGood Evening";
        }
        else if (22 >= time || time <= 24)
        {
            return "\nGood Night";
        }
    }

    int main()
    {
        cout << "What time is it? "; //ask the user for time
        int userInput; //variable to store user response
        cin >> userInput; //get user Input
        while (cin.fail()) //error handling
        {
            cin.clear();
            cin.ignore(1000, '\n');
            cout << "Invalid input. Enter the time again: ";
            cin >> userInput;
        }

        //output string returned by function
        cout << greetings(userInput) << endl;

        return 0;
    }
