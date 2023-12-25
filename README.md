# Tic-Tac-Toe Game Documentation

## Overview

This simple Tic-Tac-Toe game, developed in Java, provides a classic two-player experience where players take turns marking spaces in a 3x3 grid. The goal is to achieve three marks in a row, either horizontally, vertically, or diagonally.

## Features

### 1. Game Board

The game board is represented as a 3x3 grid, where players make their moves by selecting an empty cell to place their mark (X or O).

### 2. Player Turns

Players take turns making their moves. The game alternates between Player 1 (X) and Player 2 (O).

### 3. Win Conditions

The game checks for win conditions after each move. If a player successfully places three marks in a row (horizontally, vertically, or diagonally), the game declares that player as the winner.

### 4. Draw

If the entire board is filled, and no player has achieved three marks in a row, the game ends in a draw.


## How to Play

1. **Player 1 (X) Moves**: Click on an empty cell on the board to place an "X."
2. **Player 2 (O) Moves**: Click on another empty cell to place an "O."
3. **Winning**: Achieve three marks in a row horizontally, vertically, or diagonally.
4. **Draw**: If the board is filled with no winner, the game ends in a draw.

## Sample Code

```java
// Sample code snippet for handling player moves
for(int i=0;i<9;i++) {
  if(e.getSource()==buttons[i]) {
			if(player1_turn) {
				if(buttons[i].getText()=="") {
						buttons[i].setForeground(new Color(255,0,0));
						buttons[i].setText("X");
						player1_turn=false;
						textfield.setText("Player 2 : O's Turn");
						check();
				}
				
		}else{					
        if(buttons[i].getText()=="") {
				buttons[i].setForeground(new Color(0,0,255));
				buttons[i].setText("O");
				player1_turn=true;
				textfield.setText("Player 1 : X's Turn");
				check();
				}
    }
  }
}
