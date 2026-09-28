In essence Go is a simple game that can be played following four rules, outlined by Cho Chikun in "Go: A Complete Introduction to the Game". 

1. Stones are played on the intersections.
2. The stones do not move after being played.
3. Black plays first.
4. Black and white alternate in making their moves.

But in practice, questions arise with new players on how to functionally play and the complexity of the game has almost no bounds with the situations that can arise.

In this way, Go is an elegant game that deserves praise for it's beauty. I suggest [![this video](JRveBqnPJKg)](www.youtube.com) by Nick Sibicky on why he likes Go for a good introduction to the wonder of the game and why to even play. 

### Object of the Game

The object of the game is to control more territory than your opponent. Each unoccupied intersection of the board surrounded by a single color of stones is a point of territory. In this simple example white wins by 9 points.

<p align="center">
<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/8f765555-183a-43e8-81b2-8d837c766016" />
</p>

### Progression of Play

Black plays first and may place a stone on any intersection of the board. White and black then alternate placing a single stone on any *legal* intersection. *** More on what constitutes a legal move later.

Play continues until both players pass their turn in succession indicating they do not see any more profitable moves left. Once both players pass the game is over and ready to be [scored](#scoring). 

### Liberties and Capture

Each stone, or group of stones has what are called liberties. Liberties are the unoccupied adjacent intersections to the stone or group and can be thought of like breathing space. If every liberty is filled by a stone of the opposing color the stone suffocates and dies, or in other words is captured and removed from the board. A single stone in the middle of the board has 4 liberties. Notice the diagonal intersections are not counted as liberties. 

<p align="center">
  <img width="200" height="200" alt="image" src="https://github.com/user-attachments/assets/dcae4986-1363-4325-857c-3cf8a9c53599" />
</p>

Groups of stones share liberties. See if you can count how many liberties each group of stones has. 

<p align="center">
<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/7d781bc5-788b-4292-9de4-66daec7947aa" />
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

### Scoring
