# TicTacToe

A classic two-player TicTacToe game built in C++ for the console, featuring turn-based gameplay and automatic win detection.

## 🎮 About

This is a simple, console-based implementation of TicTacToe where two players take turns marking a 3×3 grid with X and O. The first player to align three marks horizontally, vertically, or diagonally wins the game. Perfect for learning basic C++ game development concepts.

## 🛠 Technologies Used

- **C++17** - Core programming language
- **iostream** - Standard input/output operations
- **vector** - Included for potential future enhancements

*Platform: Console Application (Windows/Linux/macOS)*

## ✨ Features

- 🎯 **Automatic Win Detection** - Checks rows, columns, and diagonals after each move
- 🤝 **Two-Player Mode** - Play with a friend on the same computer
- 🎲 **Draw Detection** - Identifies when the board is full with no winner
- ⚠️ **Input Validation** - Prevents invalid moves and occupied cells
- 🖥️ **Clean Console UI** - Visual grid representation for clear gameplay
- 🔄 **Turn Management** - Automatically switches between X and O

## ⌨️ Controls

| Input | Action |
| --- | --- |
| `0-2` (row) | Enter row coordinate |
| `0-2` (col) | Enter column coordinate |

**Game Grid Layout:**
```
(0,0) | (0,1) | (0,2)
------|-------|------
(1,0) | (1,1) | (1,2)
------|-------|------
(2,0) | (2,1) | (2,2)
```

*Example: To place X in the center, enter: `1` (row) then `1` (column)*

## 🚀 How to Run

### Prerequisites

- C++ compiler (g++, MinGW, MSVC, or IDE like Code::Blocks)
- Git (optional, for cloning)

### Compilation & Execution

1. **Clone or download** the repository:
   ```bash
   git clone https://github.com/meheru68/TicTacToe.git
   cd TicTacToe
   ```

2. **Compile the source code**:
   ```bash
   g++ -std=c++17 -o tictactoe main.cpp
   ```

3. **Run the executable**:
   ```bash
   ./tictactoe
   ```

*Alternatively, compile directly from file:*
```bash
g++ -std=c++17 main.cpp -o tictactoe
```

## 🎮 Gameplay Instructions

1. Launch the game
2. Player X moves first
3. Enter row and column numbers (0-2) when prompted
4. The game will validate your move and reject invalid inputs
5. After each move, the board is redrawn with current positions
6. The game automatically switches turns between X and O
7. When someone wins or it's a draw, the result is displayed
8. Game ends after one round - restart the program to play again

### Example Game Flow
```
   |   |   
   |   |   
___|___|___
   |   |   
   |   |   
___|___|___
   |   |   
   |   |   

Current Player is X
Enter row and column from 0-2: 1 1

   |   |   
   | X |   
___|___|___
   |   |   
   |   |   
...
```

## 💡 How It Works

### Game Loop
- The game runs for a maximum of 9 turns (one per cell)
- Each turn: display board → get input → update board → check winner → switch player

### Win Detection
The program checks for wins in three ways:
- **Rows**: Compares all three cells in each row
- **Columns**: Compares all three cells in each column  
- **Diagonals**: Checks both main diagonals (0,0→2,2 and 0,2→2,0)

### Input Handling
- Validates row/column are within 0-2 range
- Ensures selected cell is empty (' ')
- Clears invalid input from stream to prevent infinite loops

## 📚 What I Learned

- **2D Arrays** - Managing game state with a 3×3 char array
- **Input Validation** - Handling edge cases and user errors
- **Game Algorithms** - Implementing win condition checks
- **Turn-Based Logic** - Managing player state and flow control
- **Console Formatting** - Creating visual layouts with ASCII characters
- **Error Recovery** - Using `cin.clear()` and `cin.ignore()` for robust input handling

## 🔧 Potential Improvements

### Code Quality
- [ ] **Object-Oriented Design** - Create Board and Player classes
- [ ] **Remove Unused Includes** - The `vector` header is included but not used
- [ ] **Function Decomposition** - Break logic into smaller functions (drawBoard, checkWin, etc.)
- [ ] **Better Constants** - Use enums for game states instead of char winner

### Game Features
- [ ] **Replay Without Restart** - Allow multiple games in one session
- [ ] **Score Tracking** - Maintain win/loss/draw statistics across games
- [ ] **Single-Player AI** - Implement unbeatable Minimax algorithm
- [ ] **Undo Move** - Let players take back their last move
- [ ] **Save/Load Game** - Store game state to file

### Visual Enhancements
- [ ] **Clear Screen** - Add `system("cls")` or cross-platform alternative for cleaner display
- [ ] **Colored Output** - Use ANSI escape codes for player colors
- [ ] **Better Borders** - Unicode box-drawing characters (┌─┐│)
- [ ] **Position Numbers** - Show 1-9 grid labels for easier input

### Input Improvements
- [ ] **Single Number Input** - Use 1-9 positions instead of row/col pairs
- [ ] **Quit Command** - Allow 'q' to exit mid-game
- [ ] **Better Prompts** - Add "Enter row (0-2):" then "Enter column (0-2):"

### Bug Fixes & Edge Cases
- [ ] **Diagonal Logic** - Review diagonal win condition for edge cases
- [ ] **Draw Message Timing** - Ensure draw only displays when appropriate
- [ ] **Final Board Display** - Show final board state before declaring winner

## 🤝 Contributing

This is a learning project. Feel free to fork and submit pull requests for improvements!

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

**Enjoy the game!** 🎮
