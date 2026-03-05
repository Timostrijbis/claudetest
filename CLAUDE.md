# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Running the Project

Open `tictactoe.html` directly in a browser — no build step or server required.

## Architecture

Single-file vanilla HTML/CSS/JS app (`tictactoe.html`). All game logic, styles, and markup are co-located in one file.

**Game logic:**
- `board` — flat 9-element array representing the grid (index 0–8)
- `WINS` — hardcoded array of all 8 winning index triplets
- `init()` — resets board, clears DOM state, restores turn indicator
- Click handler on each `.cell` — handles moves, win detection, draw detection, and score updates
- `checkWin()` — iterates `WINS` and returns the winning triplet or `null`
- Scores (`X`, `O`, `draw`) are kept in a plain JS object and survive page reloads only within the session (no persistence)

## Workflow

After making changes, always commit and push to the GitHub repo (https://github.com/Timostrijbis/claudetest).
