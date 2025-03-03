# README
# Overview: 
This code plays a game of connect 4 for the user. If someone wins horizontally or vertically then it will tell them they won. I couldn't get it to work diagonally. If all the spaces have been used the game ends in a draw.
# Usage:
To compile this code you need a 5 methods and then the main method:
1. displayBoard() – Prints the current game board.
2. makeMove() – Allows a player to drop a piece into a column.
3. checkWinner() – Checks if a player has won the game.
4. isBoardFull() – Checks if the board is full, resulting in a tie.
5. switchPlayer()
6. main()

The first method, displayBoard(), you need to use a nested for loop that runs from 0 to the amount of columns, this loop just prints out of "|" to  signifiy a gap between spaces. Inside of the first loop you need another loop that runs from 0 to the amount of rows, this loop prints an empty space for board[i][j] for each iteration through and also another "|" after so then you have your board display.

The second method, makeMove(), takes the column the user wants to place their letter in and runs an if statement that says if the column they selected is bigger or smaller than the board then they need to pick another column. Then it has a a for loop that starts at the last row, 5, and the column the user selected. If that spot is empty then it sets it equal to the users letter, depending on whose turn it is. if that spot is not empty it keeps running the loop until theres an open spot.

The third method, checkWinner(), has 2 nested for loops and the first 1 is set to run through til i < ROWS - 3; this is because you need to check for the original spot board[i][j], then board[i+1][j] etc, to see if there are 4 in a row vertically. If there are for in a row then the user wins, if not they keep playing. The other nested for loop does the same thing but the opposite to check horizontally. I couldn't get it to work diagonallu though.

The fourth method, isBoardFull(), just does the same for loop and checks if every position is empty. If any single position is empty it returns false, meaning the game is not a draw yet.

The fifth method, switchPlayer(), does a simple if statement that says if currentPlayer is equal to 'X' then set currentPlayer = 'O'. If currentPlayer is not equal to 'X' then set currentPlayer = 'X'

The main method runs a while loop that runs until checkWinner() is false, but I don't really think that matters because in the while loop I have an if statement that says is checkWinner() is true then break out of the loop. The first thing the while loop does is calls the displayBoard(0 method to display the board. Then it asks the user to input a column, then I have another while loop after that that says if makeMove() is false, meaning the user input an invalid column, then keep running until the user inputs a valid column. Then I call the checkWinner() method and if thats true it would break the loop. If its false then the isBoardFull() method runs, and if thats true it would break the loop. If its false then it calls the switchPlayer() method and it keeps running until someone wins or the board is full.
# Author: 
Chaz Cook
# License 
I do not know what this is asking for.
