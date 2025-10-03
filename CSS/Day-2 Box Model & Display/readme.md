\*\*
first we have content, after content we have border. To give the space between content and border we give padding.
Margin is when we need to give the space between two elements or space from the screen for that element.

\*\* Margin->Border->Padding->Content
\*\* Use of Padding- so that content should not touch with border
\*\* padding: 10px 20px 30px 40px;-- Top Right Bottom Left , it works clockwise
\*\* padding: 20px 40px; -- Top bottom will be 20px , left right will be 40px
\*\* short hand notation will be same for margin
\*\* height and width will be applicable on content only.
\*\* Any content which is on website will always be in rectangular shape

\*\* Inline Element vs Block Element
-- Inline - Anchor tag, span tag - it will consume limited width, width which is necessary. 2. if there is space in above line it will start from there only. <span>Hello</span> <span>Yash</span>, both will be printed in same line. 3. We cannot apply height width on inline level elements. 4. We can apply only horizontally padding and margin on inline elements. Vertical padding and margin will show us visually only but it'll not apply.

-- Block Element - H1,p,H2 - they consume complete width, 2. they always starts with new line. 3. We can apply height width on block level elements. 4. We can apply margin and padding on block level elements

\*\* Span tag- Basically if we want to make changes for one word only in complete line span tag will help us to achieve that.

\*\* How to make block element as inline?
Use display:inline; with this block element will behave as inline in behaviour
