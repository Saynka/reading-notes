* reading notes 

chart.js, canvas 

chart.js all that you have to do is make a link to your javascript 
with the use of a CANVAS

canvas looks like a img element the difference ding that it does not have src and alt attributes 

its default size is 300px wide and 150pl tall  

Note: If your renderings seem distorted, try specifying your width and height attributes explicitly in the CANVAS attributes, and not using CSS.

having fall back content inside of a canvas tag will help on older browsers that cant render a canvas tag 

top left is 0,0 when thinking about the grid

canvas only supports two primitive shape rectangles and path (lists of  points connected bt lines)

beginPath()
Creates a new path. Once created, future drawing commands are directed into the path and used to build the path up.
Path methods
Methods to set different paths for objects.
closePath()
Adds a straight line to the path, going to the start of the current sub-path.
stroke()
Draws the shape by stroking its outline.
fill()
Draws a solid shape by filling the path's content area.

Note: When the current path is empty, such as immediately after calling beginPath(), or on a newly created canvas, the first path construction command is always treated as a moveTo(), regardless of what it actually is. For that reason, you will almost always want to specifically set your starting position after resetting a path.

Note: When you call fill(), any open shapes are closed automatically, so you don't have to call closePath(). This is not the case when you call stroke().

this is essentially how you draw mathmatically and this is complicated as shit....for now 