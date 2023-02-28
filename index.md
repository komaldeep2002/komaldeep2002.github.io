
**- WHAT IS REACT**

React is a JavaScript library for building user interfaces. It creates reusable UI components.



- Getting started with React

To get started with React, you'll need to have a basic understanding of HTML, CSS, and JavaScript. You'll also need to have Node.js installed on your computer.
Once you have Node.js installed, you can create a new React project using the create-react-app command. Here's an example:

+ npx create-react-app my-app
+ cd my-app
+ npm start

**- Why i chose this**

-First of all it is a very demanding and popular language and as for our capstone we are using this so that is one of the main reasons for me to choose this.

-Secondly,
React's declarative syntax allows developers to describe the desired state of their UI without worrying about the underlying implementation details.
And React components can be easily reused across different parts of an application, which can save time and improve code maintainability.

-Reusability of components:
Developers can reuse the components in different projects and these components can be customized I really loved that factor as i will be needing to reuse some of the components again and again to build a web application and i can customize them according to my choice in different phases.

With the help of DOM (Document Object Model) react also enhances the performance of web application. 

**-Now the question is How it works?**
So as for performance improvement react only updates the parts that have some changes instead of updating entire DOM.

To build complex UI react uses declarative programming. I just need to enter what i want to happen then react will take care of implementation which simplifies programming, reduce errors make it easy to make changes or understand the code. 

What else i have learned and noticed:
A syntax extension jsx that allows to write code like html in javascript. 

JSX File

<div>Hello </div>  

Corresponding Output

React.createElement("div", null, "Hello"); 

This creates react element and pass three arguments inside first is the name of the element which is div, second is the attributes passed in the div tag, and last is the content i.e. hello.

Why to use jsx? 

It is faster than javascript. And we can find errors in compilation state in jsx and templates can be made easily with this. It its performance by optimization 

Next i am going to explain about react components that is another interesting feature of react . It is considered and basic building blocks for react. It makes easy to make components in react. They have their own structure, methods and API’s and these can also be reused. 
 
So the components in react are of two types one is functional component which is also called stateless components so as we can understand from name that they don’t have any state 
1. function WelcomeMessage(props) {  
2.   return <h1>Welcome , {props.name}</h1>;  
3. }  

and the second one is class components these are more complex than functional components these are called stateful components because they hold state 	
class MyComponent extends React.Component {  
1.   render() {  
2.     return (  
3.       <div>component.</div>  
4.     );  
5.   }  
6. }


! Facts about react:
1. It was created by facebook in 2011
2. It is a library not a front-end framework

