# Hussin Retro Snake Classic Version

## End User Documentation and User Guide

**Hussin Retro Snake Classic Version** is a 2D browser-based Snake game inspired by the classic old Nokia phone style. The goal is simple: select a difficulty, start from **Round 1**, win each round, and try to reach and complete **Round 100**.

The game is built to run directly in the browser using HTML5, CSS, and JavaScript. No installation, account, database, or internet connection is required after opening the game file.

---

## 1. Game Objective

Your mission is to guide the snake, eat food, avoid collisions, and progress through rounds.

To become a champion, you must:

1. Start from **Round 1**.
2. Eat the required number of foods in each round.
3. Win the current round to unlock the next round.
4. Continue until you win **Round 100**.
5. Complete Round 100 to save your **Champion Difficulty**.

If you lose at any round, the current run ends.

---

## 2. How to Start the Game

### Step 1: Open the Game File

Open the game HTML file in a modern browser such as:

- Google Chrome
- Microsoft Edge
- Mozilla Firefox
- Safari

The game opens as a standalone page.

### Step 2: Select Difficulty

Before starting, choose a difficulty from the **Difficulty** dropdown:

- Easy
- Normal
- Hard
- Expert
- Legend

The selected difficulty controls the initial food requirement, snake speed, scoring bonus, and overall challenge level.

### Step 3: Click Start

Click **Start** to begin the run.

You can also start by pressing:

- The **MENU** button on the phone-style keypad
- Any keyboard arrow key
- WASD movement keys

### Step 4: Play and Win the Round

Move the snake toward the food. When you eat enough foods for the current round, you win that round and automatically move to the next round.

---

## 3. Game Flow

The game follows a strict classic progression system.

```text
Round 1
  ↓ win
Round 2
  ↓ win
Round 3
  ↓ win
...
Round 100
  ↓ win
Champion
```

If you lose:

```text
Current Round
  ↓ collision
Game Over
  ↓
New run starts again from Round 1
```

---

## 4. Winning and Losing Rules

### You Win a Round When

You eat the full required food count for that round.

Example:

```text
Food 12 / 25
```

This means you have eaten 12 foods out of 25 required foods.

When the counter reaches the required number:

```text
Food 25 / 25
```

The round is completed, and you move to the next round.

### You Lose the Run When

You lose if the snake:

- Hits the wall
- Hits its own body

When this happens, the game shows **Game Over**, saves the result, and the next run starts again from Round 1.

---

## 5. Difficulty Levels

Each difficulty has different food requirements, speed behavior, and score bonus.

| Difficulty | Round 1 Food Requirement | General Meaning |
|---|---:|---|
| Easy | 25 foods | Slowest and most forgiving mode |
| Normal | 30 foods | Balanced mode |
| Hard | 35 foods | Higher food requirement and faster movement |
| Expert | 40 foods | Advanced challenge |
| Legend | 50 foods | Highest challenge level |

---

## 6. Food Requirement System

The food requirement increases based on:

```text
Selected difficulty + Current round
```

The higher the difficulty and the higher the round, the more food you need to eat.

### Difficulty Food Growth

| Difficulty | Starts At | Food Increase Rule |
|---|---:|---|
| Easy | 25 | +1 food every 20 rounds |
| Normal | 30 | +1 food every 18 rounds |
| Hard | 35 | +1 food every 15 rounds |
| Expert | 40 | +1 food every 12 rounds |
| Legend | 50 | +1 food every 10 rounds |

### Example

For Easy difficulty:

```text
Round 1  = 25 foods
Round 21 = 26 foods
Round 41 = 27 foods
Round 61 = 28 foods
Round 81 = 29 foods
```

For Legend difficulty:

```text
Round 1  = 50 foods
Round 11 = 51 foods
Round 21 = 52 foods
Round 31 = 53 foods
```

---

## 7. Speed System

The snake speed depends on:

```text
Selected difficulty + Current round
```

The snake starts slower in early rounds and gradually becomes faster as rounds increase.

### Important

Higher speed difficulty does not mean the number shown is larger. Internally, the game uses timed movement intervals:

```text
Higher milliseconds = slower snake
Lower milliseconds = faster snake
```

The game was designed to be slower and more playable than the earlier version.

### General Speed Behavior

| Difficulty | Round 1 Behavior | Later Rounds |
|---|---|---|
| Easy | Slowest | Gradually faster |
| Normal | Moderate | Gradually faster |
| Hard | Faster | More challenging |
| Expert | Fast | High reaction requirement |
| Legend | Fastest | Maximum challenge |

---

## 8. Scoring System

The score is based on how efficiently you reach each food.

The game rewards shorter and smarter movement.

### Main Scoring Rule

```text
Fewer moves before eating food = higher score
More moves before eating food = lower score
```

### Example

If the food is close and you reach it quickly:

```text
Moves Since Food: 6
Result: Higher food score
```

If you take a long route:

```text
Moves Since Food: 40
Result: Lower food score
```

The score is calculated for every food eaten. The total round score is the sum of all food scores earned in that round.

---

## 9. Score Types Explained

The side panel shows several score and progress values.

| Field | Meaning |
|---|---|
| Current Round | The active round out of 100 |
| Difficulty | The selected difficulty level |
| Current Round Score | Score earned in the active round |
| Last Food Score | Score earned from the most recently eaten food |
| Moves Since Food | Number of snake moves since the previous food was eaten |
| Previous Round Score | Score from the last completed or lost round |
| Total Winner Score | Total score from won rounds in the current run |
| Best Reached Round | Highest round reached across saved attempts |
| Best Total Score | Highest total winner score saved in the browser |
| Champion Difficulty | Difficulty level saved after completing Round 100 |

---

## 10. Total Winner Score

The **Total Winner Score** only includes rounds that you successfully win.

If you lose during a round:

- The lost round score may appear in history.
- The lost round does not count as a completed winner round.
- The current run ends.

This makes the total score focused on successful progression.

---

## 11. Champion Difficulty

The game saves your **Champion Difficulty** only when you complete **Round 100**.

Example:

```text
You select Hard
You complete Round 100
Champion Difficulty = Hard
```

If you reach Round 50 and lose:

```text
Champion Difficulty is not updated
```

This means Champion Difficulty represents the highest meaningful achievement: completing the full 100-round challenge.

---

## 12. Controls

You can control the snake in multiple ways.

### Keyboard Controls

| Key | Action |
|---|---|
| Arrow Up | Move up |
| Arrow Down | Move down |
| Arrow Left | Move left |
| Arrow Right | Move right |
| W | Move up |
| S | Move down |
| A | Move left |
| D | Move right |
| Space | Start or pause |
| Enter | Start or pause |

### On-Screen Phone Buttons

Use the Nokia-style keypad buttons:

| Button | Action |
|---|---|
| ▲ | Move up |
| ▼ | Move down |
| ◀ | Move left |
| ▶ | Move right |
| MENU | Start or pause |

### Mouse or Touch Controls

You can also control the snake using the game screen:

- Click or tap inside the game screen to move toward that direction.
- Swipe on the screen to change direction.

This is useful for tablets and mobile screens.

---

## 13. Saved Data

The game saves progress in the browser using local storage.

Saved data includes:

- Selected difficulty
- Best reached round
- Best total score
- Champion difficulty
- Champion date
- Latest run summary
- Round history

This data stays in the same browser unless you clear it.

---

## 14. Clear Saved Scores

Click **Clear Saved Scores** to remove all saved game data from the browser.

This clears:

- Saved difficulty
- Best reached round
- Best total score
- Champion difficulty
- Saved history

Use this option only if you want to reset the game history completely.

---

## 15. Saved History

The **Saved History** section shows recent game results.

Each history item may show:

- Result type: win, loss, or champion
- Difficulty
- Round number
- Food progress
- Total moves
- Score
- Date and time

This allows the player to review previous attempts.

---

## 16. Recommended Playing Strategy

To get a higher score:

1. Avoid unnecessary movement.
2. Move directly toward the food when safe.
3. Do not rush into tight spaces.
4. Keep the snake path open.
5. Plan the next turn before reaching the food.
6. Use slower difficulties first to learn the rhythm.
7. Move to harder difficulties after mastering the controls.

---

## 17. Common Questions

### Why did I go back to Round 1 after losing?

This is intentional. The game uses classic progression rules. Losing ends the run, and a new run starts from Round 1.

### Why is my food requirement high?

The game starts with at least 25 required foods. Higher difficulties start with more food.

### Why is my score lower even though I ate the food?

The score depends on how many moves you used before eating the food. More moves reduce the food score.

### Why is Champion Difficulty still empty?

Champion Difficulty is saved only after completing Round 100.

### Can I play without internet?

Yes. After you have the HTML file, the game runs locally in the browser.

### Can I move the game to another browser and keep my saved score?

Not automatically. The saved data is stored in the browser where the game was played. Another browser or device will have separate saved data.

---

## 18. Troubleshooting

### The game does not start

Try the following:

1. Open the file in a modern browser.
2. Click inside the page.
3. Press Start or MENU.
4. Try an arrow key.

### Keyboard arrows do not work

Make sure the browser window is active. Click inside the game page, then press the arrow keys again.

### Saved scores disappeared

Possible reasons:

- You clicked Clear Saved Scores.
- Browser local storage was cleared.
- You opened the game in a different browser.
- You opened the game from a different location or origin.

### The snake is too fast

Choose an easier difficulty. Speed increases by difficulty and round.

### The snake is too slow

Choose a harder difficulty such as Hard, Expert, or Legend.

---

## 19. Browser Data and Privacy

The game does not require a login and does not send scores to a server.

All saved progress is stored locally in the browser.

The saved data is used only for game progress, score history, best score, best reached round, and champion difficulty.

---

## 20. Technical Notes for End Users

The game uses:

- HTML5 Canvas for the 2D game screen
- JavaScript for game logic and controls
- CSS for the retro Nokia-style design
- Browser local storage for saved progress

No external libraries are required.

---

## 21. Reference Links

These references explain the browser features used by the game:

- HTML Canvas API: https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API
- Browser localStorage: https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage
- KeyboardEvent key: https://developer.mozilla.org/en-US/docs/Web/API/KeyboardEvent/key

---

## 22. Version

**Game Name:** Hussin Retro Snake Classic Version  
**Guide Type:** End User Documentation and User Guide  
**Game Mode:** Classic 100-Round Champion Progression  
**Storage:** Browser Local Storage  
**Technology:** HTML5, CSS, JavaScript  
