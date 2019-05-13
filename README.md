# flipping-tiles
A visual display of a grid of tiles flipping away from the cursor position in a wave style when the mouse is clicked.

## What?

A big grid of hundreds of small tiles. When you click on one it will change color and a ripple effect will cascade over all other tiles, causing them to flip in 3D space away from the position of the cursor (the backside of each flipped tile will be the same color as the tile you clicked on). 

* The color of the wave will be chosen randomly from a set of nice pastell colors.
* Each tile should be as small as possible. Since we are calculating a ton of vectors it might end up taxing the cpu a bit to much. But the size should be atleast smaller than 20x20.

## How? 

My current idea is to draw a vector from the cursor to the center of any given tile, then measure its length to determin the delay of the flip, aka closer the tile is to the cursor the earlier it should flip. Then normalize the vector and use the (x, y) coordinates for the x and y parts of the Rotate3D transformation. This should ensure that the tile always flips "away" from the cursor, no matter where the cursor is.

## Refs: 

* Rotate3D docs: https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/rotate3d
* Rotate3D demo: https://www.w3schools.com/howto/tryit.asp?filename=tryhow_css_flip_card
* Vectors: https://en.wikipedia.org/wiki/Euclidean_vector
* Vector logic reference: ~~https://evanw.github.io/lightgl.js/docs/vector.html~~ https://jsfiddle.net/q76ohvxp/1/

## WIP

https://jsfiddle.net/r5es4uam/146/
