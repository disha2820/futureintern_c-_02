# futureintern_c-_02
#include <iostream>
#include <cstdlib> // For rand() and srand()
#include <ctime>   // For time()
using namespace std;

int main() {
    srand(time(0)); // Seed the random number generator
    int target = rand() % 100 + 1; // Generate a random number between 1 and 100
    int guess;
    int attempts = 0;

    cout << "Guess the number between 1 and 100!" << endl;

    do {
        cout << "Enter your guess: ";
        cin >> guess;
        attempts++;

        if (guess > target) {
            cout << "Too high! Try again." << endl;
        } else if (guess < target) {
            cout << "Too low! Try again." << endl;
        } else {
            cout << "Congratulations! You guessed it in " << attempts << " attempts." << endl;
        }
    } while (guess != target);

    return 0;
}
