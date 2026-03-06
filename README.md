# Python Game Development: Guess the Number Game

## Project Overview

This project is a simple interactive **Guess the Number** game built using Python. The program generates a random number within a selected range, and the player must guess the correct number before running out of attempts.

The game tracks statistics during the session and calculates scores based on difficulty level and remaining attempts.

---

## How the Game Works

1. The player enters their name.
2. The program displays the **game instructions and scoring system**.
3. The player chooses a **difficulty level**:

   * **Easy** → numbers between 1–50, 15 attempts, multiplier ×1
   * **Medium** → numbers between 1–100, 12 attempts, multiplier ×2
   * **Hard** → numbers between 1–500, 10 attempts, multiplier ×4
4. The computer generates a **random secret number** within the chosen range.
5. The player guesses the number. After each guess the game provides feedback:

   * **Too High**
   * **Too Low**
6. The player continues guessing until:

   * the number is guessed correctly, or
   * the player runs out of attempts.

After each round, the player can decide whether to **play again**.

---

## Scoring System

The score for each round depends on how many attempts remain when the correct number is guessed.

**Score Formula**

Score = (Remaining Attempts + 1) × Difficulty Multiplier

Example:

* Easy difficulty with 2 attempts remaining
  Score = (2 + 1) × 1 = 3

* Hard difficulty with 0 attempts remaining
  Score = (0 + 1) × 4 = 4

The score from each round is added to the **session score**.

---

## Game Statistics

The program tracks statistics during each session, including:

* Games Played
* Games Won
* Games Lost
* Average Attempts per Game
* Best Round Score

At the end of the session, these statistics are displayed to the player.

---

## Input Validation

The program includes several forms of input validation to prevent errors:

* Player name must contain letters only
* Guesses must be numeric values
* Guesses must be within the allowed range
* Difficulty selection must be 1, 2, or 3
* Play-again responses must be yes or no

Invalid inputs are handled gracefully with appropriate error messages.

---

## Technologies Used

* Python 3
* "random" module (for generating the secret number)

---

## Project Structure

The program is organised into several functions:

* `get_player_name()`
  Validates and returns the player's name.

* `show_instructions()`
  Displays the rules and scoring system.

* `choose_difficulty()`
  Allows the player to select the game difficulty.

* `get_valid_guess()`
  Validates the player's guesses.

* `calculate_score()`
  Calculates the score for each round.

* `play_game()`
  Runs a single round of the game.

* `ask_to_play_again()`
  Handles replay logic and confirmation.

* `show_statistics()`
  Displays session statistics.

* `main()`
  Controls the overall flow of the game.

---

## Possible Future Improvements

Some features that could be added in the future include:

* graphical interface (GUI) using Tkinter or Pygame
* difficulty levels with adaptive scoring
* persistent statistics saved to a file
* sound effects or animations

