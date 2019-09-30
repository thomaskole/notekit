# This Fork
The fork serves as a proof-of-concept for intergrated ruler functionality in Notekit.
The rulers are available seamlessly, and allow the user to freehand draw various geometric lines, all while in freehand draw mode.

# Cartesian ruler
the Cartesian (x-y) ruler is available under *shift*.
While holding down shift, the user chooses a direction by drawing left-right or up-down. The cursor is then limited to the start x- or y-value.

![Cartesian example](/screenshots/cartesian-example.gif?raw=true)

# Polar ruler
The polar ruler allows the user to draw arbirary diagonal lines, or circles like a compass. This functionality is available under *ctrl*.
When you press this button, a center point is placed.
Like the cartesian ruler, the polar ruler chooses a direction based on the first move. Away or towards the center results in a diagonal line, parallel to it results in a circle.

![Polar example](/screenshots/polar-example.gif?raw=true)

# Possible improvements

## Polar feedback
There is not enough feedback to the user about the *Polar ruler* mode. A cross could be drawn on the center location when *ctrl* is held, and a bit of information could be shown about distance.
This makes the compass feel more like an actual compass, too.

![Polar example](/screenshots/compass-support.png?raw=true)

## Vector math
A simple vector math library would be very helpful, and would make the code a lot more readable

## Direction decision
Right now, both rulers immediately choose a direction upon moving the cursor.
While using a mouse, this seems to result in predictable movement, but the jitter of a graphics tablet makes this less predictable.
Sometimes you end up drawing horizontal where you meant to be drawing vertical, and vice-versa. Same goes for the Polar ruler.
