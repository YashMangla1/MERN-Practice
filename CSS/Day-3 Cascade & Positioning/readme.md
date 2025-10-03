\*\* If we were trying to give any property to an element like background-color property to H1 Element through inline css,internal css and externall css but it'll give first preference to inline css only

\*\* if we give internal and external css to an element, but condition is in HTML file we are writing first internal CSS and then external CSS link. so it'll give priority to external CSS. but if we have external css link first and then internal styling it'll give priority to internal css styling.

\*\* if we apply any css property by selecting that tag and by class , it'll give priority to class and if we also select it through id, it'll give highest priority to id.

\*\* multiple elements can have same class but multiple elements cannot have same id. Mutiple elements can have same tag but id will always be unique.

\*\* Order of Priority for CSS= 0. !important 1. Inline CSS(Priority high) 2.Id(Priority) 3. Class 4: Tag(h1,h2) 5. ordering is important when it's tie between class, tag or anyting

\*\* if we have to give priority to external css only then we need to use !important to override the inline css

\*\* Positioning in CSS

1. static - it'll be same as original one
2. relative: relative means basically it'll apply the properties respective to its original position
3. Fixed- it will fix the component like we have navigation bar, it'll be fixed relative to the window.
4. Sticky- lets take an example of github, when we open a repo and scroll below a nav bar automatically sticks to the top, that is sticky. Basically when top is 0px or whatever we fix the top accordingly it'll get sticky.
5. Absolute- basically it'll leave it's own space and other element will take that place. this element will be free. but we're setting up the top and left. How it'll take that - basically if the ancestor is relative,sticky or fixed it'll take position on behalf of them otherwise corresponding to browers window.

\*\* in relative, at thier original position no other element come and take that space. it'll be empty only. but in fixed original position can be taken by other elements if we change the original position of fixed element.
