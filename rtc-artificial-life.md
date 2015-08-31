<permalink>rtc-artificial-life</permalink>
<month>5</month>
<year>2015</year>

# Collaborative artificial life

I have always been fascinated with artificial life and decided to make my own real-time collaborative cellular automaton in Node.js. More specifically I wanted to bring the magic of real-time collaboration to the Conway's Game of Life so that every single user that loads the game will be interacting with the same board.

The Game of Life was created by the British mathematician John Conway. In an attempt to find an "self-replicating machine" Conway drastically simplified the an earlier automaton by John von Neumann which contained several complex rules. The Conway's model [appeared on the page 120 of the 1970's issue of the Scientific American] and made him instantly famous.

Most of the cellular automatons ahve very simple rules, here is a simple example of these mathematical models work:

Let's say we have a chessboard grid and a bunch of pawns which we will call a *living cell* from now on. If there is a *living cell* on the board that grid square is considered to be alive, if there is not living cell then that square is considered to be dead.

These two states are can be easily represented on a computer by using the binary system, so that the equivalence ends up being **1 for a living cell** and **0 for a dead cell**.

Now image that you throw 5 living pawns on the 8x8 board and you end up in the following pattern:

[image]

This is called the generation 0, to compute the next generation we will follow these 4 rules:

*1.- Any living cell with fewer than two live neighbors dies, as if caused by under-population.
2.- Any living cell with two or three live neighbors lives on to the next generation.
3.- Any living cell with more than three live neighbors dies, as if by overcrowding.
4.- Any dead cell with exactly three living neighbors becomes a living cell, as if by reproduction.*

By applying these simple rules we end up with the next generation which looks like this:

[image]

You will notice that successive generations will make the pattern move away from where it started, this pattern will eventually perish when it reaches the border of the chessboard.

[animation]

This example is one of several, many, many structures that create different results. You can try them on a real chessboard or a piece of paper, or you could simply use the project I made [here].

That’s it! With some really simple rules you end up having an living ecosystem (hmm well and artificially living ecosystem).

This is how the finished project looks like:

[]

Click on the image to load the Game of Life and play with it creating some structures, don't forget to set your nickname! Note that **the app is real-time collaborative**, every user is actually seeing and interacting with the same board, I made it this way to see how it evolves with time, I plan to leave running this project running for a looong time...