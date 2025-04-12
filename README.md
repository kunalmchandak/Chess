# ♟️ Chess

A Python-based chess game with AI opponent support, built using **Pygame**. The game allows both **human vs. human** and **human vs. AI** modes.

---

## Features
- Play **human vs. human** or **human vs. AI**.
- AI uses **Negamax with Alpha-Beta pruning** for better performance.
- Supports **legal chess moves, castling, en passant, and pawn promotion**.
- **Undo moves** and **reset the game** using keyboard shortcuts.
- Graphical chessboard with piece movement animations.

---

## How to Run the Game
### **1️⃣ Install Dependencies**
Ensure you have **Python** installed, then install **Pygame**:
```bash
pip install pygame
```

### **2️⃣ Run the Chess Game**
```bash
python ChessMain.py
```

---

## Configuring AI and Human Players
By default, both players are **human-controlled**. You can enable AI for **one or both players**.

In **ChessMain.py**, find these lines:
```python
playerOne = True  # True = Human plays White, False = AI plays White
playerTwo = True  # True = Human plays Black, False = AI plays Black
```
Change them to:
- **Human vs AI (AI as Black)**
  ```python
  playerOne = True  # Human plays White
  playerTwo = False  # AI plays Black
  ```
- **AI vs Human (AI as White)**
  ```python
  playerOne = False  # AI plays White
  playerTwo = True   # Human plays Black
  ```
- **AI vs AI (Both AI-controlled)**
  ```python
  playerOne = False  # AI plays White
  playerTwo = False  # AI plays Black
  ```

---

## How the AI Works
The AI uses **Negamax with Alpha-Beta Pruning**, which:
1. **Searches possible moves** up to a certain depth.
2. **Prunes unnecessary branches** to speed up decisions.
3. **Scores board positions** based on material advantage.

To adjust AI difficulty, modify **DEPTH** in `AI_player.py`:
```python
DEPTH = 3  # Increase for stronger AI, decrease for faster but weaker AI
```

---

## Controls
- **Move pieces:** Click on a piece, then click on a valid destination square.
- **Undo last move:** Press `Z`.
- **Reset game:** Press `R`.

---

## License
This project is open-source and available for free use and modification.

---

## Contributing
If you’d like to contribute or improve the AI, feel free to fork the repository and submit a pull request!


