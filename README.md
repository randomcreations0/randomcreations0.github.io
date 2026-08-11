# WORDSHIFT

**Change one letter. Find the path.**

A daily word ladder puzzle game. Transform the START word into the TARGET word by changing exactly one letter at a time. Every intermediate word must be a valid English word.

## How to Play
a
1. You're given a **START** word and a **TARGET** word of the same length
2. Change exactly one letter to form a new valid English word
3. Keep going until you reach the TARGET word
4. Try to do it in the fewest moves possible!

**Example:**
```
COLD
 ↓
CORD
 ↓
CARD
 ↓
WARD
 ↓
WARM
```

## Features

- **Daily Puzzle** — New puzzle every day, same for everyone
- **Practice Mode** — Play unlimited puzzles at Easy, Medium, or Hard difficulty
- **Challenge Mode** — Find the shortest path
- **Hints** — Get help when you're stuck (Next Letter, Next Word, Full Path)
- **Statistics** — Track your wins, streaks, and move distribution
- **Dark Mode** — Easy on the eyes, day or night
- **Share Results** — Share your score without spoiling the solution
- **Responsive** — Works great on desktop, tablet, and mobile
- **Accessible** — Keyboard navigation, screen reader support

## Running Locally

1. Clone or download this repository
2. Open `index.html` in any modern web browser
3. No server required — everything runs in the browser

```bash
# If you have Python installed:
python3 -m http.server 8000
# Then open http://localhost:8000

# If you have Node.js installed:
npx serve .
# Then open the shown URL
```

## Deploying to GitHub Pages

1. **Create a new repository** on GitHub (e.g., `wordshift`)

2. **Upload all project files:**
   - `index.html`
   - `style.css`
   - `game.js`
   - `words.js`
   - `README.md`

3. **Enable GitHub Pages:**
   - Go to your repository's **Settings** tab
   - Scroll down to the **Pages** section
   - Under **Source**, select **Deploy from a branch**
   - Choose **main** branch and **/(root)** folder
   - Click **Save**

4. **Access your game:**
   - Your game will be live at: `https://yourusername.github.io/wordshift/`

### Updating the Game

1. Edit the files locally
2. Commit and push to the `main` branch
3. GitHub Pages will automatically update (may take a minute)

## Project Structure

```
wordshift/
├── index.html      # Main HTML file
├── style.css       # All styles (light & dark themes)
├── game.js         # Game logic, UI, state management
├── words.js        # English word list for validation
└── README.md       # This file
```

## Technical Details

- **No backend** — Pure client-side JavaScript
- **No external dependencies** — No frameworks, no APIs
- **Deterministic daily puzzles** — Same puzzle for everyone on the same date
- **BFS pathfinding** — Guarantees optimal solution calculation
- **localStorage** — Saves your progress and statistics locally
- **System fonts** — No external font dependencies

## How Daily Puzzles Work

The daily puzzle is determined solely by the calendar date:

1. Days since January 1, 2026 are calculated
2. A seeded pseudo-random number generator uses this value
3. The generator selects a word pair and verifies it's solvable
4. The optimal path length becomes the Par score

Every player on the same date receives the exact same puzzle, regardless of browser, device, or account.

## License

Copyright © 2026 randomcreations0

Wordshift is open source and may be freely used, copied, modified, and redistributed, provided that **credit is given to the original creator, randomcreations0**.

You may:

* Use the code for personal or commercial projects
* Copy and modify the code
* Create and distribute derivative versions
* Host your own version of Wordshift
* Include portions of the code in other projects

### Attribution Requirement

If you use, copy, modify, or redistribute substantial portions of Wordshift, you must credit the original creator:

> **Wordshift by randomcreations0**

You must retain this copyright and attribution notice in copies or substantial portions of the software.

You may not claim the original Wordshift project or its original code as your own.

This software is provided "as is", without warranty of any kind. The original creator is not responsible for any damages or issues arising from its use.
