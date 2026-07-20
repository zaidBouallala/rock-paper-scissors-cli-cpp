# Rock Paper Scissors CLI

A simple command-line Rock Paper Scissors game built with C++. The player competes against the computer for up to 10 rounds. The program generates random computer choices, evaluates each round, tracks the score, changes the console color based on the result, and announces the final winner.

## Features

- Play between 1 and 10 rounds
- Choose Stone, Paper, or Scissors
- Random computer choices
- Displays the result of every round
- Tracks player wins, computer wins, and draws
- Announces the overall game winner
- Changes the Windows console color based on the result:
  - Green when the player wins
  - Red when the computer wins
  - Yellow when the round is a draw

## Technologies

- C++
- Standard C++ Library
- Windows console commands

## Requirements

The game uses the Windows `color` command through `system()`, so its colored feedback is designed for Windows terminals.

You need one of the following:

- Visual Studio with the **Desktop development with C++** workload
- MinGW-w64 with `g++`
- Another C++ compiler that supports C++11 or later

## Build and Run

### Using g++

```bash
g++ main.cpp -o rock-paper-scissors
rock-paper-scissors.exe
```

### Using Visual Studio

1. Create a new **Console App** project.
2. Replace the generated source code with the code from `main.cpp`.
3. Build the solution.
4. Run the application.

## How to Play

1. Enter the number of rounds you want to play, from 1 to 10.
2. For each round, select one of the available choices:
   - `1` for Stone
   - `2` for Paper
   - `3` for Scissors
3. The computer randomly selects its choice.
4. The game displays both choices and announces the round winner.
5. After all rounds, the game displays the final score and overall winner.

## Game Rules

- Stone beats Scissors
- Scissors beats Paper
- Paper beats Stone
- Identical choices result in a draw

## Example

```text
How many rounds 1 to 10?
3

Your Choice: [1]:Stone, [2]:Paper, [3]:Scissors ?
1
---------------Round [1]---------------
Player choice: Stone
Computer choice: Scissors
Round Winner: Player

             GAME OVER

Total Rounds: 3
Player Wins: 2
Computer Wins: 1
Draws: 0
Game Winner: Player
```

## Suggested Project Structure

```text
rock-paper-scissors-cli-cpp/
├── main.cpp
├── README.md
├── LICENSE
└── .gitignore
```

## Known Limitations

- The score counters are global variables.
- Invalid non-numeric input is not handled yet.
- The colored console feedback depends on Windows commands.
- The game ends after one match and does not currently offer a replay option.
- The `RoundLength()` function is defined but not used.

## Possible Improvements

- Add an option to play again
- Reset score counters before every new match
- Validate non-numeric input
- Replace global counters with a structure
- Make console colors cross-platform
- Simplify the winner logic
- Add ASCII art for Stone, Paper, and Scissors
- Store match history or high scores
- Separate the game logic into source and header files
- Add unit tests for the game rules

## Author

**BOUALLALA ZAID**

## License

This project is available under the MIT License. Add a `LICENSE` file if you want to publish it under MIT.
