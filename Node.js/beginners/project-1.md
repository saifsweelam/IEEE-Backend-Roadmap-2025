## JavaScript Task Obligation: Interactive CLI Hangman Game

### Overview
This task is designed for JavaScript learners to apply their understanding of basic concepts and object-oriented programming (OOP) principles in a fun and interactive way. The focus is on creating a command-line interface (CLI) game that allows users to play Hangman.

### Task Description
You are tasked with creating an interactive CLI Hangman game. The game will select a random word, and the player will have a limited number of attempts to guess the letters in the word. The game will provide feedback after each guess, indicating whether the guess is correct or incorrect, and display the current state of the word with guessed letters filled in.

### Requirements

#### Hangman Class
- Create a `Hangman` class with the following properties:
  - `wordList` (array) - An array of words to choose from
  - `word` (string) - The randomly selected word
  - `attempts` (number) - Number of attempts the player has
  - `guesses` (array) - Array to store the player's guessed letters
  - `currentState` (string) - The current state of the word with guessed letters and underscores for unguessed letters

- Include methods:
  - `selectRandomWord()` - Selects a random word from the `wordList` and sets the `word` property.
  - `initializeGame()` - Initializes the game state by resetting attempts, guesses, and `currentState`.
  - `makeGuess(letter)` - Takes a letter from the player, adds it to the `guesses` array, updates the `currentState`, and returns feedback ('correct', 'incorrect', or 'already guessed').
  - `isGameOver()` - Returns true if the player has used all attempts or guessed the word correctly.
  - `getCurrentState()` - Returns the current state of the word with guessed letters and underscores for unguessed letters.
  - `play()` - Runs the interactive game loop using console inputs and outputs.

### Deliverables

* JavaScript code file containing the Hangman class.
* A README file explaining how to run the application and examples of its usage.

### Evaluation Criteria
* Correct implementation of the Hangman class.
* Proper use of OOP principles, including encapsulation.
* Clear and concise code with appropriate comments and documentation.
* Functional and correct implementation of all required methods.
User-friendly and interactive CLI experience.