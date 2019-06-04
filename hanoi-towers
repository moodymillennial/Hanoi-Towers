////////////////////////////////////////////////////////////////////////////////////////////////
// Joshua Stromberg
// Input: User enters number of disks they want for the game Towers of Hanoi
// Output: Either "Not valid try again" OR "Working... Move disk X from X to X... Took X Moves"
// Process: Uses global variables to store counts, void and main functions, loops to keep game
//          going, and recursive functions.
////////////////////////////////////////////////////////////////////////////////////////////////
 
#include <iostream>
#include <fstream>
using namespace std;
 
// pattern to solve the game!
// for my reference while I code:
// move disc 1 A to C ACB
// move disc 2 A to B ABC
// move disc 1 C to B CBA
// move disc 3 A to C ACB
// move disc 1 B to A BAC
// move disc 2 B to C BCA
// move disc 1 A to C ACB
 
// start with globals, moves start at 0, so do disks
int moves = 0;
int disks = 0;
void solveAndMoveHanoi(int disks, char fromPole, char withPole, char toPole);
 
// main function
int main(){
    // ask user for how many disks
    int discs;
    cout << "Enter the number of discs: " << endl;
    cin >> discs;
    // if disks is less than or equal to 1 the user will be prompted over and over to enter a different number
    while (discs <= 1)
    {
        cout << "Invalid entry try again" << endl;
        cout << "Enter the number of discs: " << endl;
        cin >> discs;
        continue;
    }
    // if number entered is valid program starts moving the disks
    cout << "Working..." << endl;
    solveAndMoveHanoi(discs, 'A', 'B', 'C');
    // program prints the amount of moves the program took
    cout << "It took " << moves << " moves. " << endl;
    return 0;
}
 
// this function solves the hanoi tower and moves the disks
void solveAndMoveHanoi(int disks, char fromPole, char withPole, char toPole){
    // number of moves increases by 1 for each step
    moves++;
    // couldn't get program to work at disks == 0, but using disks == 1 for last move worked perfect
    // this just prints out where the disk is moved to
    if(disks == 1){
        cout << "Move disc " << disks << " from " << fromPole << " to " << toPole << endl;
    }
    // formula for moving disks from one place to another if we aren't on the last disk
    else{
        solveAndMoveHanoi(disks-1, fromPole,toPole,withPole);
        cout << "Move disc " << disks << " from " << fromPole << " to " << toPole << endl;
        solveAndMoveHanoi(disks-1,withPole,fromPole,toPole);
    }
}
