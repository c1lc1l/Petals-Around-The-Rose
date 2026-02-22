# Petals Around the Rose – README

This is a self‑contained HTML game for **"Petals Around the Rose"**, a classic logic puzzle where players must deduce the scoring pattern from dice rolls.  
The game simulates rolling five dice and challenges you to guess the hidden score.

---

## Overview

`Petals Around the Rose` is a browser‑based puzzle game in a single HTML file with embedded CSS and JavaScript.  
Roll dice, enter your guess, and discover if you figured out the pattern.  
The score is always **zero or an even number**—your mission is to work out *why*.

---

## How to Run

1. Save the code as `petals-around-the-rose.html`.
2. Open the file in any modern browser (Chrome, Firefox, Safari, etc.).
3. No installation, server, or dependencies needed.

---

## Features

- Five animated dice with realistic 3×3 dot grid rendering.
- Smooth roll animations, hover effects, and visual feedback.
- Responsive design for desktop and mobile devices.
- Modern glassmorphism UI with gradients and custom typography.
- Enter key support for quick guessing.
- Clear correct/wrong feedback with congratulatory message for winners.

---

## How to Play

1. Click **"Roll Dice"** to generate a new roll.
2. Study the five dice and enter your guess for the score.
3. Click **"Accept Guess"** (or press Enter).
4. See if you're correct! If wrong, the correct score is revealed.
5. Roll again and refine your pattern recognition.
6. Consistently correct guesses make you a **Pentate of the Rose** 🌹.

---

## Code Structure

**HTML Layout:**
- `.container`: Centered glass card with header, game area, and rules.
- Dice container, number input, buttons, and result box.
- Rules section with "How to Play" instructions.

**CSS Styling:**
- Gradient background with radial glows.
- Glassmorphism card (backdrop blur, transparency, shadows).
- Playfair Display (titles) + Poppins (body) fonts.
- Responsive grid layout.
- Dice as 3×3 grids with `.dot` elements.
- Animations: slideDown/Up, float, rollDie.

**JavaScript Logic:**
- Initializes 5 dice with empty 3×3 grids.
- `rollDice()`: Generates random 1–6 values, animates dice, enables guessing.
- `getDotDisplay(number)`: Renders correct dot positions for each face.
- `checkGuess()`: Validates input, compares to calculated score, shows feedback.
- Event handlers for buttons and Enter key.

---

## 🔐 **SPOILER: The Secret Rule** (Read after playing!)

> **The scoring rule:** Count the "petals around the rose" (dots that are *not* in the center).
> 
> Only odd‑numbered dice (1, 3, 5) have "petals":
> 
> | Dice Face | Petals | Explanation |
> |-----------|--------|-------------|
> | 1         | 0      | Single center dot (no petals around it) |
> | 2         | 0      | No petals |
> | **3**     | **2**  | Center + 2 corner dots (2 petals) |
> | 4         | 0      | No petals |
> | **5**     | **4**  | Center + 4 corner dots (4 petals) |
> | 6         | 0      | No petals |
> 
> **Score = Sum of petals across all 5 dice.** Always even or zero.

Example: Dice showing 3, 1, 5, 2, 5 → Petals: 2 + 0 + 4 + 0 + 4 = **10**.

The `calculateScore()` function implements exactly this logic.

---

## Credits

Based on the classic "Petals Around the Rose" puzzle.
