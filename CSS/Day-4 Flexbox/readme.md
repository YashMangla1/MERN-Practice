\*\* Flexbox in CSS
Parent - Child relation is very important
Parent - conatiner
Child- Flex item

\*\* We have four child elements which are block elements but we took the parent and give the property display:flex, becuase of which child elements will come in one single line.
\*\* Another property is flex-direction which is by default is row but when we set this to columne all child will arrange column wise.

\*\* Another property row-reverse and column-reverese, it will reverse the child elements like fourth to first, both column and row wise.

\*\* justify-content will always work around main axis. When flex-direction is column, cross axis will be main axis and main axis will be column axis. Main axis will always be decided by flex-direction

\*\* align items always work with cross axis. basically justify-content and align items work together but justify-content will always apply on horizontal axis which is basically X-axis and align-items will always work on cross axis which is Y-axis

\*\* flex-wrap:wrap means it makes our element responsiveness.

\*\* if we have extra space and we give flex-grow as 1, it'll take all the available space.
flex-grow:1, flex-grow:2- how these will work it will divide the empty available space in three parts , 2 parts willl be given to second one and 1 part will be given to first one

\*\* flex shrink, if we lower down the resolution, so all the elements wills shrink proportionally but if we give flex-shrink:4 to any particular element then that element will shrink first 4x more compared to others.

\*\* flex-basis:200px , if we have given the width then flex-basis will override the width. flex-basis will have higher priority. it will work around main axis , if it's row wise then width and flex is column then width will increase.

\*\* align-self: flex-start; what this will do is if we have 4 elements center aligned but we want to move one element to top we'll use align-self

\*\* We can use align-content to set how multiple lines are spaced apart from each other. This property takes the following values:

flex-start: Lines are packed at the top of the container.
flex-end: Lines are packed at the bottom of the container.
center: Lines are packed at the vertical center of the container.
space-between: Lines display with equal spacing between them.
space-around: Lines display with equal spacing around them.
stretch: Lines are stretched to fit the container.

This can be confusing, but align-content determines the spacing between lines, while align-items determines how the items as a whole are aligned within the container. When there is only one line, align-content has no effect.

\*\* The two properties flex-direction and flex-wrap are used so often together that the shorthand property flex-flow was created to combine them. This shorthand property accepts the value of the two properties separated by a space.

For example, you can use flex-flow: row wrap to set rows and wrap them.

\*\* The frogs are all squeezed onto a single row of lilypads. Spread them out using the flex-wrap property, which accepts the following values:

nowrap: Every item is fit to a single line.
wrap: Items wrap around to additional lines.
wrap-reverse: Items wrap around to additional lines in reverse.

\*\* Sometimes reversing the row or column order of a container is not enough. In these cases, we can apply the order property to individual items. By default, items have a value of 0, but we can use this property to also set it to a positive or negative integer value (-2, -1, 0, 1, 2).

\*\* Flex-direction
row: Items are placed the same as the text direction.
row-reverse: Items are placed opposite to the text direction.
column: Items are placed top to bottom.
column-reverse: Items are placed bottom to top.
