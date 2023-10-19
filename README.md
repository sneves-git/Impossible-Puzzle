# <p align="center">Problem A - Impossible puzzle!</p>
### Description
Would you like to win 1 million pounds? That was the question posed by Christopher Monckton when he launched the Eternity puzzle, in June 1999 (see Figure 1). The prize was offered to the first person who could solve this tilling puzzle, during the next 4 years. The puzzle was solved in May 2000 by two mathematicians from Cambridge, Alex Selby and Oliver Riordan, who happily cashed their prize!

<p align="center">
  <img src=https://i.imgur.com/x43yRgO.png /><br>
  Figure 1 - Eternity puzzle.
</p>

In 2007, Christopher Monckton created a new version of the game (Eternity 2), and with it a new competition. The new prize was 2 million dollars, again with a time horizon of 4 years. In 2011, the deadline passed without any solution been found. Moreover, no known solution has been published up until today! You can no longer win the 2 million dollars, but you can still go down in history as the person who solved the "unsolvable" Eternity 2!

Eternity 2 is an edge-matching puzzle, where squared pieces are placed in a 16 x 16 board. When placing a piece, each of the four edges must connect with a piece with the same color on the contacting edge (it is not really just a color, is a figure combining a shape and a color, but we will call it a "color" for simplicity). No orientation is pre-defined, so a piece can be rotated in any direction to be placed in the board. A special case is the boarder pieces, so there is a specific edge color (grey) to the limits of the board, as you can see in Figure 2.

<p align="center">
  <img src=https://i.imgur.com/U44nRc4.png /><br>
  Figure 2 - Eternity 2 puzzle.
</p>

But do not fear, we do not expect you to solve this puzzle! We will just warm you up so you can solve it in the future!

A similar puzzle is the Danger puzzle. This puzzle has the same characteristics as the the Eternity 2 puzzle, but the "colors" are in the corners and not in the edges. So a edge is, in practice, a combination of two colors. See Figure 3 with an example.

A difference here is that there are no boarder "color", so each piece can be or not in the limits of the board.

<p align="center">
  <img src=https://i.imgur.com/lOqBCPA.png /><br>
  Figure 3 - Danger puzzle.
</p>

Your objective is to solve a set of "Danger puzzles" of different board sizes, and report the solution.

For each puzzle, you will be given the number of pieces (N), the size of the board (rows R and columns C), and a list of the N pieces to use. Each piece is represented by 4 integers, each integer representing a color. The four colors represent the colors of each corner of the piece, in clockwise order, starting by the top left corner (see Figure 4). As explained, each piece can be placed in any possible rotation, so for each piece there are 4 possible configurations.

Special case: First piece.

The first piece of the input is a special case. That piece can be placed directly in the first position of the board (top-left corner), with the configuration as it comes from the input. This is an anchor piece, which you are given to start your solution upon. See the examples below.

<p align="center">
  <img src=https://i.imgur.com/FsHG0QH.png /><br>
  Figure 4 - Piece configurations.
</p>

##
### Input
The input starts with one line containing the number of test cases.

Then, for each test case, the first line contains three numbers: 1 ≤ N ≤ 2500, 1 ≤ R ≤ 50 and 1 ≤ C ≤ 50. N represents the number of pieces provided, and R and C are the size of the board, corresponding to the number of rows and columns, respectively. Notice that N = R * C.

After that, N lines follow, corresponding to the N pieces. Each of the N lines contains 4 integer values, corresponding to the colors of the four corners of the piece, as described in Figure 4. The value of each corner color ranges between 0 and 999. There are no repeated pieces, meaning each of the N pieces is unique.
##
### Output
For each test case, you should print the solution board as in the example below, or the phrase 'impossible puzzle!\n' if no solution can be found. For the solution board, leave two spaces between peaces in the same row and an empty line between rows of the board. Inside each piece, leave one space between columns in the same row (See Figure 5).

<p align="center">
  <img src=https://i.imgur.com/953YPrp.png /><br>
  Figure 5 - Solution.
</p>

##
### Example
#### Example input:
3<br>
3 1 3<br>
2 5 1 3<br>
1 5 4 5<br>
3 2 5 4<br>
2 2 1<br>
1 2 3 4<br>
4 1 3 4<br>
4 2 2<br>
1 2 3 4<br>
1 3 2 5<br>
4 2 3 1<br>
5 4 3 2<br>

#### Example output:
2 5__5 4__4 3<br>
3 1__1 5__5 2<br>
impossible puzzle!<br>
1 2__2 5<br>
4 3__3 1<br>

4 3__3 1<br>
5 2__2 4<br>

##
### NOTE
In output the "_" represents a space