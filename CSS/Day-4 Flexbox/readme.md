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
