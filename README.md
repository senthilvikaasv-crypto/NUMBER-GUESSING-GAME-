# NUMBER-GUESSING-GAME-
USED TO PLAY A GAME WHERE WE GUESS THE NUMBER 

#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main() {

    srand(time(0));

    int secret = rand() % 100 + 1;
    int guess;
    int attempts = 0;

    cout << "===== NUMBER GUESSING GAME =====" << endl;
    cout << "Guess a number between 1 and 100" << endl;

    while (true) {

        cout << "Enter your guess: ";
        cin >> guess;

        attempts++;

        if (guess > secret) {
            cout << "Too High! Try again." << endl;
        }
        else if (guess < secret) {
            cout << "Too Low! Try again." << endl;
        }
        else {
            cout << "Congratulations! You guessed it!" << endl;
            cout << "Attempts: " << attempts << endl;
            break;
        }
    }

    return 0;
}
