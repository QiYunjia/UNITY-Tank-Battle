# UNITY-Tank-Battle

"Tank Battle" Game Description  

1. Unity Version  
   · 2022.3.53f1c1  

2. Enemy Behavior Strategy:  
   · Regular Tank  
    - Movement Speed: 2  
    - Behavior:  
        * Uses random movement pattern, changes direction every 4 seconds  
        * Immediately turns upon encountering obstacles  
        * Fires a straight bullet every 3 seconds  
        * Deals 1 damage upon collision with the player (1-second cooldown)  

   · Enhanced Tank (AI Tracking Type)  
    - Movement Speed: 3  
    - Behavior:  
        * Intelligently tracks the player's position, prioritizing movement along the X or Y axis  
        * Higher attack frequency, fires a bullet every 2 seconds  
        * Deals 1 damage upon collision with the player (1-second cooldown)  
        * Special Mechanism:  
            - Switches back to random movement if the player is out of range  

3. AI Tool Usage  
   · Deepseek was used for code organization and debugging  

4. Additional Notes  
Game Overview  
"Tank Battle" is a classic top-down shooter where players control a tank to battle enemies on the battlefield, using shooting and tactical maneuvers to evade enemy attacks. The game combines random and AI tracking enemy behaviors, offering diverse combat experiences. Players must strategically utilize shooting skills, map resources, and power-ups to eliminate all enemies and survive. As the game progresses, players can take on higher difficulty challenges for more intense battles.  

Controls  
   · Supports keyboard (WASD/arrow keys for movement, Space to pause, Shift to sprint) and mouse (left-click to shoot).  

Game Rules  
   · Victory Condition: Defeat all enemies.  
   · Defeat Condition: Player's health drops to zero.  

Main Menu  
   · Start:  
    - New players automatically enter Easy Mode on their first playthrough.  
    - After completing Easy Mode, clicking "Start" directly enters Hard Mode.  
   · Settings:  
    - Adjust background music volume.  
    - Toggle game sound effects on/off.  
    - Set game difficulty.  
   · Leaderboard:  
    - Stores scores and completion times for each game session.  
    - Displays the top three scores and times on the leaderboard.  
   · Credits:  
    - Developer's name, student ID, email, and date.  
   · Exit:  
    - Opens a confirmation window.  
    - Confirming exits the game; canceling returns to the main menu.  

Game Scene  
   · Map:  
    - Indestructible Obstacles: Can be destroyed by enemy or player bullets, randomly distributed across the map.  
    - Destructible Obstacles: Cannot be destroyed by bullets, randomly placed within and around the map.  
    - Enemies:  
        * Can be eliminated by player bullets.  
        * Includes two enemy types, with a maximum of 10 enemies on the map.  
        * When defeated, enemies display an explosion effect and respawn at random positions.  
    - Player:  
        * Moves using WASD, sprints with Left Shift, and shoots with left mouse click.  
        * Can fire bullets to destroy enemies and destructible obstacles.  
        * Loses health when hit by enemy bullets or colliding with enemies.  
        * Can collect dropped items from obstacles to gain abilities.  
    - Item Drops:  
        * Blood Packs and Firepower spawn randomly every 3 seconds.  
        * Items rotate in place and disappear when collected by the player.  
        * Blood Pack restores 1 health point.  
        * Firepower enables automatic bullet firing for 3 seconds (0.2-second interval).  

Game States  
   · Player Status: Displays score, health, and elapsed time on the left side of the map.  
   · Victory: Shows "Victory," player score, and completion time, with options to enter Hard Mode, restart, or return to the main menu.  
   · Defeat: Shows "Game Over," with options to restart or return to the main menu.  
   · Pause: Press Space to pause, with options to resume, restart, or return to the main menu.  
