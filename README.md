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
