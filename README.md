# Brick Breaker
This is a simple brick breaker game written in Java. The game is played by using the mouse to move a paddle at the bottom of the screen. The player must hit the bricks with the paddle to break them. If all of the bricks are broken, the player wins.

# How to Play
*Run the Main.java file.
*Use the mouse to move the paddle at the bottom of the screen.
*Hit the bricks with the paddle to break them.
*If all of the bricks are broken, the player wins.
Controls
*Left click: Move the paddle left
*Right click: Move the paddle right

# License
This project is licensed under the MIT License. See the LICENSE file for more information.

## Code Explaination
### Main.java
The code is written in Java and it creates a simple brick breaker game. The code starts by importing the necessary libraries, namely `javax.swing`, `java.awt`, and `java.awt.event`.

The next step is to create the `Main` class. This class contains the main method, which is where the game is executed. The main method first creates a `JFrame` object, which is the window that will be used to display the game. The `JFrame` object is then given a title, a size, and a visibility. It is also set to not be resizable.

The next step is to create a `GamePlay` object. This object is responsible for the actual game logic. The `GamePlay` object is then added to the `JFrame` object.

Finally, the `main` method calls the `setDefaultCloseOperation` method on the `JFrame` object. This method specifies what happens when the user closes the window. In this case, the program will exit.
The code belongs to the `brickPong` package.

```
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;
```
Importing the necessary libraries. The `javax.swing` library provides classes for creating graphical user interfaces. The `java.awt` library provides classes for working with basic graphics. The `java.awt.event` library provides classes for handling events, such as mouse clicks and keyboard presses.

```
JFrame obj = new JFrame();
```
Creates a `JFrame` object. This object is the window that will be used to display the game.

```
GamePlay gamePlay = new GamePlay();
```
Creates a `GamePlay` object. This object is responsible for the actual game logic.

```
obj.setBounds(10, 10, 700, 600);
```
Set the bounds of the `JFrame` object. The bounds specify the position and size of the window.

```
obj.setTitle("Brick Breaker");
```
Sets the title of the `JFrame` object. The title 'Brick Breaker' will be displayed in the title bar of the window. 

```
obj.setResizable(false);
```
This prevents the user from resizing the window.

```
obj.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
```
Specifies what happens when the user closes the window. In this case, the program will exit.

```
obj.add(gamePlay);
```
Adds the `GamePlay` object to the `JFrame` object. This will cause the `GamePlay` object to be displayed in the window.

### MapCreator.java
The code creates a class called `MapCreator`. This class is responsible for creating and drawing the bricks in a brick breaker game. The class has three public methods:

* `MapCreator(int row, int col)`: Creates a new `MapCreator` object with the specified number of rows and columns.
* `draw(Graphics2D g)`: This method draws the bricks to the screen.
* `setBrickValue(int value, int row, int col)`: Sets the value of the brick at the specified row and column.

The `MapCreator` class uses a two-dimensional array to store the bricks. The `row` and `col` parameters of the `MapCreator` constructor specify the number of rows and columns in the array. The `draw()` method iterates through the array and draws each brick to the screen. The `setBrickValue()` method sets the value of the brick at the specified row and column to the specified value.

The `MapCreator` class is a reusable class that can be used to create bricks in any brick breaker game.

### Gameplay.java
 This class is responsible for the game logic of the brick breaker game. The class has following members:

* `play`: A boolean variable that indicates whether the game is in play.
* `score`: An integer variable that stores the current score.
* `totalBricks`: An integer variable that stores the number of bricks remaining.
* `timer`: A `Timer` object that is used to control the game loop.
* `delay`: An integer variable that specifies the delay between each iteration of the game loop.
* `playerX`: An integer variable that stores the x-coordinate of the paddle.
* `ballposX`: An integer variable that stores the x-coordinate of the ball.
* `ballposY`: An integer variable that stores the y-coordinate of the ball.
* `ballXdir`: An integer variable that stores the x-direction of the ball.
* `ballYdir`: An integer variable that stores the y-direction of the ball.
* `map`: An object of the `MapCreator` class. This object is used to create and draw the bricks.

The `GamePlay` class has the following methods:

* `paint()`: This method draws the game on the screen.
* `actionPerformed()`: This method is called by the timer object to iterate the game loop.
* `keyPressed()`: This method is called when a key is pressed.
* `keyReleased()`: This method is called when a key is released.
* `moveRight()`: This method moves the paddle to the right.
* `moveLeft()`: This method moves the paddle to the left.

The `GamePlay` class is highly reusable and customizable.
