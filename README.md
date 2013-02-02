#Dropblox AI

This is an AI program that will autonomously play a Tetris variant. 
We developed it in the Dropblox AI Competition on Dec 2, 2013.
[https://playdropblox.com/]

It was written in Python.

The AI was divided into three parts.
First, find every possible final positions. Then rate all these positions and sort them by ratings. Finally, find path to the best position we've got.

The rating mechanism is like this: 
rating = (-1.0) * landingHeight + ( 1.0) * erodedPieceCellsMetric
         + (-1.0) * boardRowTransitions + (-1.0) * boardColTransitions
         + (-4.0) * boardBuriedHoles 　  + (-1.0) * boardWells;
