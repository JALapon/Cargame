# Car Game

## Description
This is a simple console-based car game written in C++. The player controls a car that moves left and right to avoid incoming enemy cars. The game runs inside a terminal window and utilizes Windows-specific console functions to render graphics and handle user input.

## Features
- **Simple Graphics**: Utilizes ASCII characters to represent cars and the game environment.
- **User Input Handling**: Players can move their car left or right using the 'A' and 'D' keys.
- **Scoring System**: Increases the score when the player successfully avoids enemy cars.
- **Collision Detection**: Ends the game when the player's car collides with an enemy car.
- **Game Over Screen**: Displays a game over message and prompts the user to return to the menu.
- **Instructions Screen**: Provides guidance on how to play the game.
- **Menu System**: Allows the player to start the game, read instructions, or exit.

## How to Play
1. **Start the Game**: Run the executable and select `1. Start Game` from the menu.
2. **Move the Car**: Use the following keys:
   - Press `A` to move left.
   - Press `D` to move right.
   - Press `ESC` to exit the game.
3. **Avoid Enemies**: Steer your car to avoid the incoming enemy cars.
4. **Game Over**: If your car collides with an enemy car, the game ends and displays the final score.

## Installation and Compilation
### Requirements
- A Windows operating system (since the game uses Windows-specific functions)
- A C++ compiler (e.g., MinGW g++, MSVC)

### Compilation Steps
1. Open a command prompt and navigate to the directory containing the source file.
2. Compile the program using the following command (for MinGW g++):
   ```sh
   g++ car_game.cpp -o car_game.exe -std=c++11
   ```
3. Run the game:
   ```sh
   car_game.exe
   ```

## Code Explanation
### Important Functions
- **`gotoxy(int x, int y)`**: Moves the console cursor to a specified location.
- **`setcursor(bool visible, DWORD size)`**: Adjusts the visibility and size of the console cursor.
- **`drawBorder()`**: Draws the game boundaries.
- **`genEnemy(int ind)`**: Generates enemy cars at random positions.
- **`drawEnemy(int ind)`**: Draws an enemy car on the screen.
- **`eraseEnemy(int ind)`**: Removes the enemy car from the screen.
- **`resetEnemy(int ind)`**: Resets an enemy car when it moves out of bounds.
- **`drawCar()`**: Renders the player's car.
- **`eraseCar()`**: Removes the player's car from its current position.
- **`collision()`**: Checks for collisions between the player's car and enemy cars.
- **`gameover()`**: Displays the game over message and prompts the player to return to the menu.
- **`updateScore()`**: Updates and displays the player's score.
- **`instructions()`**: Shows the game instructions.
- **`play()`**: Contains the main game loop, handling user input, enemy movement, and collision detection.
- **`main()`**: Implements the main menu, allowing the user to start the game, view instructions, or exit.

## Possible Improvements
- **Cross-Platform Compatibility**: Modify the code to work on Linux/macOS by replacing Windows-specific functions.
- **Enhanced Graphics**: Use a graphical library like SDL or SFML for better visuals.
- **Additional Features**: Add power-ups, different levels, or multiplayer support.
- **Dynamic Difficulty**: Increase enemy speed as the score increases.

## License
This project is open-source and can be freely modified or distributed. No warranty is provided.

