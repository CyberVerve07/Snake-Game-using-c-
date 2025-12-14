# Snake-Game-using-c++

# Snake Game in C++ 🐍

A classic Snake game implemented in **C++** using the legacy **`graphics.h` (WinBGIm)** graphics library.  
Control the snake with your keyboard, eat fruits to grow, and avoid colliding with the walls or your own body.

> This project is mainly for learning basic game logic, arrays/vectors, and simple 2D graphics in C++.

---

## 📌 Features

- Simple and lightweight C++ project.
- Uses **WinBGIm / graphics.h** for 2D graphics rendering. [web:1][web:2]
- Keyboard controls using `W`, `A`, `S`, `D`.
- Score system that increases when you eat a fruit.
- Snake grows longer each time it eats.
- Game over when:
  - The snake hits the wall.
  - The snake hits its own tail.

---

## 🧱 Game Rules

- You start with a short snake and a score of `0`.
- A red fruit appears at a random position on the grid.
- Each time the snake's head reaches the fruit:
  - The score increases by `1`.
  - The snake length (`lengthmax`) increases.
  - A new fruit is spawned at another random valid position.
- If the snake:
  - Touches the borders of the game window, **you lose**.
  - Touches any part of its own body (tail), **you lose**.
- After losing, the game shows your final score and waits for a key press before closing the window.

---

## 🛠 Tech Stack

- **Language**: C++
- **Graphics Library**: `graphics.h` (WinBGIm) [web:1][web:10]
- **Compiler**: MinGW / TDM-GCC or any Windows GCC that supports WinBGIm
- **Recommended IDEs**:  
  - Code::Blocks  
  - Dev-C++ (or Orwell Dev-C++) [web:12][web:15]

-
Make sure your IDE still knows where `graphics.h` and `libbgi.a` are (from the installation step).

### 4. Build & Run

- Click **Build** or **Compile & Run** from the IDE.
- A window titled `SnakeGame` should open.
- Start playing using your keyboard.

---

## 🎮 Controls

- `W` – Move Up  
- `A` – Move Left  
- `S` – Move Down  
- `D` – Move Right  

You cannot directly reverse direction (e.g., going right and instantly pressing left) to avoid instant self-collision.

---

## 🧠 How It Works (Quick Overview)

- The snake’s **head position** is stored as `(x1, y1)`.
- The **tail positions** are stored in two `std::vector<int>`:
  - `snakex` for the x-coordinates
  - `snakey` for the y-coordinates
- On each frame:
  - The current head position is pushed to the front of the tail vectors.
  - The tail is trimmed to match the current length (`lengthmax`).
  - Keyboard input (`w/a/s/d`) updates the direction.
  - The head moves one step (10 pixels) in that direction.
  - Collision with fruit increases score and length, and spawns a new fruit.
  - Collision with wall or tail ends the game.

This keeps the logic simple and easy to read for beginners.

---

## 🧪 Possible Improvements

Some ideas you can add later:

- Difficulty levels (change `delay()` to make the snake faster). [web:8]
- Pause / resume functionality.
- High-score saving to a file.
- Better UI: start menu, restart button, etc.
- Port the logic to a modern framework like **SFML**, **SDL2**, or **raylib** for cross-platform support. [web:23][web:29]

---

## 📄 License

Open to everyone

---

## 🙌 Acknowledgements

- Inspiration from classic Snake games.
- General references and tutorials 


