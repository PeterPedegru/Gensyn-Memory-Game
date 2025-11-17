GENSYN MEMORY

A stylish 'memory game' (find a pair) in the GENSYN sci-fi style. 3 difficulty levels, time/move tracking, and high score saving.

This is a classic memory training game, fully implemented in a single index.html file. It requires no build process or external libraries and runs in any modern browser.

🚀 Features

Three difficulty levels:

Level 1: 4 Pairs (8 cards)

Level 2: 8 Pairs (16 cards)

Level 3: 16 Pairs (32 cards)

Stat Tracking: The game counts the number of moves (Moves) and total time (Time).

"Smart" Timer: The timer only starts on the first card click, not on page load.

High Score Saving: The best time and minimum moves are saved in your browser's localStorage for each level.

Stylish Design: A minimalist sci-fi dark theme with an accent color and the Space Mono font.

Responsive: The game displays correctly on desktop and mobile devices.

All in One File: All logic, styles, and structure are in a single index.html file.

🎮 How to Play

Press 'Start New Game' to begin from Level 1.

Click on the cards to flip them over.

Find two matching images in a row. If they match, they stay open.

If the images don't match, they will flip back over.

Clear the board of all pairs to complete the level and advance to the next.

Your goal is to complete all levels with the minimum time and moves.

🛠️ How to Run

No web server is required to run this game.

Download the index.html file.

Create a folder named images in the same directory as index.html.

Place your 17 image files (1.png, 2.png, 8.jpg, etc.) into the images folder.

Open the index.html file in any web browser (Chrome, Firefox, Safari, etc.).

🔧 Customization

You can easily customize the game by editing index.html.

1. Changing Images

Find the arts array in the <script> tag:

const arts = [
  "images/1.png", "images/2.png", "images/3.png", "images/4.png", 
  "images/5.png", "images/6.png", "images/7.png", "images/8.jpg",
  "images/9.png", "images/10.png", "images/11.png", "images/12.png",
  "images/13.png", "images/14.png", "images/15.png", "images/16.png",
  "images/17.png"
];


You can change the file paths, add new ones, or remove old ones. The game will automatically adapt to the number of images in this array.

2. Adjusting Levels

Find the levelConfigs object in the <script> tag:

const levelConfigs = {
  1: 4,  // Level 1: 4 pairs
  2: 8,  // Level 2: 8 pairs
  3: 16  // Level 3: 16 pairs
};


You can change the number of pairs for each level or add new levels. Important: Make sure the maximum number of pairs (here 16) does not exceed the total number of unique images in the arts array (here 17).

3. Changing Colors and Style

All main colors are defined as CSS variables at the beginning of the <style> tag. You can easily change them:

:root {
  --bg-color: #0a0a0a;      /* Main background */
  --card-bg: #230800;     /* Card and modal background */
  --accent-color: #fad7d1; /* Text and accent color */
}


💻 Tech Stack

HTML5 (Semantic Markup)

CSS3 (Flexbox, Grid Layout, Transitions, Custom Properties)

JavaScript (ES6+) (DOM Manipulation, Game Logic, localStorage)
