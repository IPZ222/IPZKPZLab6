# IPZKPZLab6
# Tic-Tac-Toe

A console-based Tic-Tac-Toe game implemented in C# using design patterns. This project features a human player vs. computer player setup, with an option to restart the game after each match.

## Features

- Human vs. Computer gameplay
- Observable pattern to update the game board display
- Factory pattern for player creation
- Single-instance game manager (singleton pattern)
- Game reset functionality for multiple rounds

## Project Structure
TicTacToe

Core
- Board.cs: Represents the game board.
- Player.cs: Abstract player class.
- HumanPlayer.cs: Human player implementation.
- ComputerPlayer.cs: Computer player implementation.
- PlayerFactory.cs: Factory for creating players.
- GameManager.cs: Singleton game manager to control game flow.
- IObserver.cs: Interface for observer pattern.
- ConsoleBoardObserver.cs: Console-based observer to display the game board.
- Program.cs: Entry point for the application.

## Programming Principles Used
1. Single Responsibility Principle (SRP)
Each class in the project has a single responsibility. For example, the Board class handles the game board, Player and its derived classes handle player behavior, and GameManager handles game flow.
2. Open/Closed Principle (OCP)
The code is open for extension but closed for modification. New player types can be added by extending the Player class without modifying existing code.
3. Liskov Substitution Principle (LSP)
Derived classes such as HumanPlayer and ComputerPlayer can be used interchangeably with the base class Player without affecting the program's correctness.
4. Interface Segregation Principle (ISP)
The IObserver interface ensures that only the required methods are implemented by the observers, promoting a clean and focused interface.
5. Dependency Inversion Principle (DIP)
High-level modules like GameManager do not depend on low-level modules; instead, both depend on abstractions such as Player and IObserver.
6. Design Patterns
Singleton Pattern: Used in GameManager to ensure only one instance controls the game flow.
Factory Pattern: Used in PlayerFactory to create player instances based on type.
Observer Pattern: Used to update the console display whenever the game board changes.
