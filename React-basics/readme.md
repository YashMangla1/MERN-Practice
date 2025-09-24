React- it is an external library that helps us create website easier.

HTML code- create a website

How do we load JS onto our website?
1.using HTML <script> element, this tag can load contet from anywhere on the internet. 2. save a JS code in a file

External Library- code that is outside of our computer, someone else wrote but we can load this code on our website and use it. Eg- React is and external library.

<script src="https://unpkg.com/supersimpledev@8.6.4/external-library.js"></script>

We're using two url's for React in our code because react can be used in different places.
React=shared features
React-dom= features specific to websites

Using React to create websites
Load React and ReactDOM

Using React to create apps
Load React and React-native

const container = document.querySelector(".js-container");
We're using querySelector to get an HTML element(.js-container) from the website and put it into our Javascript.
This is a featire of JS called the DOM, basically JS gives the document object which sort of combines JS and HTMl together. it gets HTML elements from the page and put them into our JS and also lets our JS modify HTML elements on the page. Document combines HTML and JS together.

ReactDOM.createRoot(container).render(
"Welcome to SuperSimpleDev React Course"
);
ReactDOM.createRoot= Basically sets up React
to set up an react we need to give an HTML element

(container)- this element going to act as a container, everything thay we create with React is going to be displayed inside this container class element. The reason react uses a container is because it keeps things organized and isolated.

.render- lets us to display inside the container.

What is babel?
it is an JS compiler, translates other languages to JS.
When using React we do not use normal JS, we use JSX
JSX- javascript XML, same js JS but we can write HTML directly in our JS code.

1. JSX helps us to detect errors easier.
2. JSX helps us to insert values inside JSX elements, using <p>hello{2+2}</p>
3. Our webbrowser does'nt understands JSX, we use babel to translates JSX into normal JS.

<script type="text/babel"> this code tells to translates all text to JS.

Q) What if we need to render the multiple elements in React?
We cannot add multiple elements inside one variable, also we cannot pass multiple elements inside the render function.
We use div element, it acts like a container in HTML. div is one element and it stored in one variable which is supported in JS.


Lesson - 2 
Component, Props, destructuring and guard operator(&&)

Component- it's a piece of the website, it's better to split into componenets and work on each component.
-Components are designed to reuse. eg- ChatMessage
Component name must start with Capital letter. i.e. PascalCase
JSX is more stricter, we need to close each HTML element
<ChatInput></ChatInput> - component Syntax
We're creating our own element ChatInput and we can use our own HTML elements and build the websites.

- We're using multiple div's in our HTML Code which is not practice we can remove those divs using something in React called as Fragment(<></>)
-instead of div word we'll use them empty , basically this will group the elements together and extra div won't be entered, basically those will be removed from the code.
<div> is an block element, block element take up an entire line by itself, here fragment won't work because we need to display the text on next line. layout purpose we use div only.

***
Props make our component reusable
We can add our own attributes to the components, but how we access it inside this component and use it? we do that using a feature called props. Every component function gets one parameter up here called props.
This props parameter is an object and it contains all the attributes that we give to the component . We get 'message' attribute and it has a value "hello chatbot". Attribute name is saved as property and attributes values saved as value of the property.
props=properties, we called this props because the attributes are saved as properties in this object.
We can add multiple attributes to the component.{message, sender}
--        const message = props.message;
          const sender = props.sender;
          const { message, sender } = props; //this way is called destructuring, we're taking stuff out of this object(i.e. props), we're destructuring it
          it takes us to take properties directly out of an object.

--       function ChatMessage({ message, sender })- This takes the message and sender properties directly out of the first parameter and saves them in thier individual variables.

function ChatMessage(props) - this is old way

-- Guard operator(&&)- const result= value1 && value2
    if value1 is true, the result will be value2
    this works just like an if statement.

-- Best practice is to use a Component to create the app function App(){return(html code)};
render(<App/>)


Lesson -3 State
-it makes our website interactive
-let us add new chat messages to our website.

step-1 :first we need to save the data in the variables. data=information, data- message and sender
Step-2: Generate the HTML

{}- save the result of the code into the prop
''- save the value of the code into the prop

-Error: Each child in a list should have a unique key prop. In, react if we insert an array of components, we need to give each component a prop called key. The key helps React track changes in the array.
