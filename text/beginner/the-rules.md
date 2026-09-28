In essence Go is a simple game that can be played following four rules, outlined by Cho Chikun in "Go: A Complete Introduction to the Game". 

1. Stones are played on the intersections.
2. The stones do not move after being played.
3. Black plays first.
4. Black and white alternate in making their moves.

But in practice, questions arise with new players on how to functionally play and the complexity of the game has almost no bounds with the situations that can arise.

In this way, Go is an elegant game that deserves praise for it's beauty. I suggest [this video](https://youtu.be/JRveBqnPJKg?si=IAHkVObHF0mYjilb) by Nick Sibicky on why he likes Go for a good introduction to the wonder of the game and why to even play. 

### Object of the Game

The object of the game is to control more territory than your opponent. Each unoccupied intersection of the board surrounded by a single color of stones is a point of territory. In this simple example white wins by 9 points.

<p align="center">
<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/762fbc72-f528-4340-82ae-2f7700426110" />
</p>

### Progression of Play

Black plays first and may place a stone on any intersection of the board. White and black then alternate placing a single stone on any *legal* intersection. *** More on what constitutes a legal move later.

Play continues until both players pass their turn in succession indicating they do not see any more profitable moves left. Once both players pass the game is over and ready to be [scored](#scoring). 

### Liberties and Capture

Each stone, or group of stones has what are called liberties. Liberties are the unoccupied adjacent intersections to the stone or group and can be thought of like breathing space. If every liberty is filled by a stone of the opposing color the stone suffocates and dies, or in other words is captured and removed from the board. A single stone in the middle of the board has 4 liberties. Notice the diagonal intersections are not counted as liberties. 

<p align="center">
  <img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/9f6d1017-cd75-470c-b8e0-43f96884288c" />
</p>

Groups of stones share liberties. See if you can count how many liberties each group of stones has. 

<p align="center">
<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/fe1557d3-5d47-494a-85d6-cd77c6843991" />
</p>

<details>
  <summary>Answers</summary>
 A: 8, B: 8, C: 5
</details>

Here are examples of captured stones. As soon as white plays the marked stones, the black stones are captured and will be removed from the board.

<p align="center">
<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/212667e1-11af-49de-b066-8c52f40f9b9c" />
</p>

Here is the resulting board state: 

<p align="center">
<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/6aabef6d-6e9f-4fb5-a2cb-b56c46755ac7" />
</p>

A side note: before white plays the capturing marked stones the black stones have only 1 liberty left each and are said to be in atari. When your stones are in atari, they can be captured on your opponents next move unless measures are taken against such actions.

When you capture a stone it becomes a prisoner and should be set aside. At the end of the game prisoners deduct from your opponents score. 

### Illegal Moves

#### No Suicide 
It is illegal in Go to play a move where your stone is dead on landing. For example, the point marked A is an illegal move for black. This is because the black group will have no liberties left if the point is filled. 

<p align="center">
<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/04f4c621-9bb5-4051-9cf7-db58a85ffbc6" />
</p>

However, if your move will make a capture it is legal to play into a space where you will have no liberties. The act of capturing stones creates liberties for the stone being placed. On this board, the point "A" is now a legal move for black.

<p align="center">
<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/a2892914-233b-4881-839f-b5e122d8e1fa" />
</p>

#### No Repeating A Previous Board State

The rule is that no arrangement of stones on the board may exist for more than one move during the game. The board state must change. 

This rule arises from a situation called ko. In ko the problem is, if allowed, players could capture each other back and forth an infinite number of times resulting in a loop that breaks the game. To resolve this problem, we observe that a previous board state may not be repeated. 

In practice it looks like this. A ko is created when black plays A. Notice white can now capture black at B.

<p align="center">
<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/fe08b6ee-a9b3-4b06-8851-ccc268fa5924" />
</p>

If white decides to play the ko and capture at B, can black now capture white back at C?

<p align="center">
<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/5c5617fc-0905-4140-a940-85a149d8f613" />
</p>

<details>
  <summary>Answer</summary>
 No
</details>

Because the board has already been in that position, playing at C is not an option for black this turn. Black must play elsewhere on the board or pass their turn. This gives white options. First white may choose to fill the ko, stopping the madness.

<p align="center">
<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/098c2ee7-2da2-4d6f-9871-5bf793ff444b" />
</p>

Otherwise if white decides there is a more pressing move on the board elsewhere, they are free to play it. This leaves the ko in play. Because the board state has now changed, black may now come back and recapture white in ko. 

### Scoring

Here we will learn Japanese (territory) scoring. There are other methods of scoring that result in the same score or similar by a narrow margin. 

At the end of a game dead stones are removed from the board and added to captures. More on this in the next section, "Living and Dead Groups". Next, captures are used to fill in the territory of their respective color. Stones may now be rearranged while preserving borders between colors, to make easier shapes to count. It is preferable to make boxes with dimensions of 5 or 10, but any formation is acceptable as long as you can count the number of intersections accurately. 

[An example 9x9 game](https://online-go.com/demo/1785676) presented by Cho Chikun in "Go: A Complete Introduction to the Game" can be viewed at OGS. There is a second branch that shows how it could be counted. Comments are on the last node of each branch. For full professional commentary on the game, please consider purchasing the book. 

### Other Rules

#### Komi

Because black getting the initiative to move first is an advantage, white is often awarded bonus points called komi to make up for the deficit. Standard komi under Japanese rules is 6.5 points. Why the 0.5? This is a tie breaker. In the event of a tie, white wins. 

#### Handicap

Players are frequently not the same strength. To equalize the difficulty of a game between players of different ranks we use a handicap system. With a handicap, the weaker player takes black and starts with anywhere from two to nine stones on the board at the start of the game that rest on the star points. One stone typically represents a single rank difference between players. White then gets to make the first autonomous move. Komi is set to 0.5 as a simple tie breaker. 

#### Time Keeping (Byo-yomi)

If playing with a clock, standard Japanese time keeping has a main time (e.g. 45 minutes), then when the main time is all used up you enter byo-yomi. In byo-yomi you will have five periods of 30 seconds left in which to make moves. If you do not use the full 30 seconds in a period the time for that period is reset. The last 10 seconds of a period will be counted aloud. If all of your byo-yomi periods are used up, you will lose on time. 


