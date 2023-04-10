---
layout: default
---

<link rel="stylesheet" type="text/css" href="style.css">

<style>
h1 {
  background-color: white;
}
h2 {
  background-color: white;
}
h3 {
  background-color: white;
}
</style>

# **Reacting To React**
![Alt text](/react-app-1.png)

# **Creating React App**
## **what i have discussed in my last blog**
React JS was developed by Facebook and released as an open-source project in 2013. It has since gained popularity among developers due to its simplicity and scalability. React JS is a popular JavaScript library used for building user interfaces. 

It is known for its ability to create dynamic and interactive web applications with ease. One of the key benefits of React is its ability to create reusable components, which can save developers time and reduce code duplication. React also has a large and active community, which means there are plenty of resources available for learning and troubleshooting. In addition to building web applications, React can also be used for building mobile applications using frameworks such as React Native. This allows for code reuse between web and mobile applications, making development more efficient. 

React also has a feature called virtual DOM, which allows for faster rendering of changes to the UI. When a component's state changes, React updates the virtual DOM, which is a lightweight representation of the actual DOM. React then calculates the difference between the old and new virtual DOM and updates the actual DOM only where necessary. React can be used with a variety of other libraries and frameworks, such as Redux for state management and React Router for routing. This makes React a versatile tool for building complex web applications. 

In this blog post, we will explore the basics of React JS by building a simple maths calculator. We will cover the key concepts of React JS such as components, state, and props, and how they are used to create interactive UI elements. 
In React, components are the building blocks of UI elements. They are reusable pieces of code that can be used to create complex UIs. Components can be either functional or class components. State is a built-in object in React that allows components to store and manage data. State is used to keep track of the current values of variables that can change over time. When state changes, the component is re-rendered to reflect the new values. Props, short for properties, are used to pass data from a parent component to a child component. Props are read-only and cannot be modified by the child component. Props are used to customize the behavior of a child component and make it more dynamic. To create interactive UI elements in React, you can use state and props to manage the data and functionality of the component. For example, you can create a button component that displays a count and increments the count when clicked.

## **Setting Up the React Environment**
Before we begin, we need to set up the React environment. We will be using Create React App, a tool created by Facebook for setting up a new React project. The first step in setting up the React environment is to install Node.js. Node.js is an open-source, cross-platform, back-end JavaScript runtime environment that executes JavaScript code outside of a web browser. It includes npm, the Node Package Manager, which is used to install and manage third-party packages or libraries that are needed for a project. Once we have Node.js installed, we can use the command line interface (CLI) to run a command that creates a new React project using Create React App. Create React App is a command-line tool that generates a starter kit for a React project. It sets up the development environment with all the necessary configuration files and dependencies pre-installed. Now, we can open our terminal and run the following command:

## **npx create-react-app math-calculator**
The command npx create-react-app math-calculator creates a new React project called "math-calculator" in our current directory. This command will take a few minutes to complete as it downloads all the necessary dependencies and sets up the project files. Once the command finishes, we will have a new folder called "math-calculator" in our directory. Finally, we can open the project in our preferred text editor, such as Visual Studio Code. Visual Studio Code is a free and open-source code editor developed by Microsoft. It has built-in support for JavaScript, React, and many other programming languages and frameworks. Opening the project in our text editor will allow us to start building our math calculator using React.

## **Building the UI Components**
The first step in building our maths calculator is to create the UI components:
Before we start coding the logic for our calculator, we need to create the user interface (UI) components. UI components are visual elements that users interact with, such as buttons, text boxes, and displays. These components will define the structure and behavior of our calculator, and will be reusable across different parts of our code.
In React, a component is a reusable piece of code that defines the structure and behavior of a UI element.a component is a building block of a user interface. It is a self-contained piece of code that defines the appearance and behavior of a UI element, and can be reused throughout the application. Components can have properties that are used to customize their appearance and behavior, and they can also have internal state that can change over time.

We will create two components: Display and Keypad:
In our calculator, we will create two components: Display and Keypad. The Display component will display the result of the calculations, and the Keypad component will contain the buttons for performing the calculations.

The Display component will display the result of the calculations:
The Display component will be responsible for displaying the output of the calculator. It will take a prop (a piece of data passed from the parent component) that represents the current result of the calculation, and render it to the screen.

The Keypad component will contain the buttons for performing the calculations:
The Keypad component will be responsible for displaying the buttons for performing the calculations. It will also define the behavior for when these buttons are clicked, such as updating the state of the calculator to perform the appropriate calculation.

## **Display Component**
In React, components can be defined using either class or function syntax. In this case, we are defining a functional component called Display.

A functional component is simply a JavaScript function that returns a React element. In this case, the Display function takes a single prop called result. This prop will be passed down from the parent component and will contain the current result of the calculations. In this file, we will define the Display component. The code for the Display component is as follows:
![Alt text](/1.png)

In the code above, we have imported the React library and defined a functional component called Display. The Display component takes a prop called result, which is the current result of the calculations. The component returns a div with a class of display, which contains an h2 element that displays the current result.
The return statement in the function returns a div element with a className of display. Inside the div, there is an h2 element that displays the value of the result prop.

By defining the Display component in this way, we have created a reusable UI element that can display the current result of our calculations. We can now use this component in other parts of our application by passing the current result as a prop.

## **Keypad Component**
Next, we will create the Keypad component. We will create a new file called Keypad.js in the src folder of our project. In this file, we will define the Keypad component. The code for the Keypad component is as follows:
![Alt text](/2.png)

In the code above, we have imported the React library and defined a functional component called Keypad. The Keypad component takes a prop called handleClick, which is a function that handles the button clicks. This prop is passed down from the parent component, which is the Calculator component that we will create later. When a button is clicked, it triggers the handleClick function with the button's value as an argument.The component returns a div with a class of "keypad", which contains the buttons for performing the calculations. We have defined the buttons using JSX syntax. JSX is a syntax extension to JavaScript that allows you to write HTML-like code in your JavaScript.
We have used a loop to generate the buttons dynamically. The loop creates an array of button values and maps over the array to generate the buttons. We have added event handlers to the buttons that call the handleClick function when the button is clicked.
Overall, the Keypad component is responsible for rendering the buttons and passing the button values to the parent component's handleClick function when a button is clicked.
## **Creating the App Component**
In React, the App component is typically the top-level component of a React application. It is responsible for rendering all the other components of the application. In this case, our App component will render the Display and Keypad components.

To create the App component, we will define a functional component called App in a new file called App.js within the src folder of our project. We will import the Display and Keypad components into this file and use them within the App component's return statement.

Once the App component is defined, we can then render it to the DOM using the ReactDOM.render method in our index.js file. This will display the entire application on the web page. The code for the App component is as follows:
![Alt text](/3.png)

In the code above, we have imported the React library and defined the App component. The App component uses the useState hook to define a state variable called result, which is initially set to an empty string. The component also defines a function called handleClick, which handles the button clicks. The handleClick function checks if the button clicked is the equals sign (=) or the clear button (C). If the button clicked is the equals sign, the function uses the eval() function to evaluate the expression and update the result. If the button clicked is the clear button, the function resets the result to an empty string. If any other button is clicked, the function appends the button to the result. The App component returns a div with a class of app, which contains the title of the calculator, the Display component, and the Keypad component. The handleClick function is passed to the Keypad component as a prop.

The App component is then exported as the default export of the module using the export default syntax. This allows other modules in the project to import and use the App component. We can now import the App component into the index.js file and render it to the DOM using the ReactDOM library. With this, we have completed the development of our math calculator app. We can now run the app and start using it to perform various mathematical calculations.

## **Styling the Calculator**
Finally, we can add some styles to our calculator to make it look more visually appealing. We will create a new file called App.css in the src folder of our project. In this file, we will define the styles for the calculator. The code for the App.css file is as follows:
![Alt text](/4.png)

## **Creating the Calculator Component**
Now that we have set up the basic structure of our application, let's move on to creating the Calculator component.We will create a new file called Calculator.js in the src folder of our project. In this file, we will define the Calculator component. The component will render the App component, which in turn will render the Display and Keypad components. We will also import the App.css file to apply the styles to the calculator. Finally, we will export the Calculator component so that it can be used in other parts of our application. This component will handle all the logic related to the calculator and display the result on the screen. Here's how we can create the component:
![Alt text](/5.1.png)
![Alt text](/5.2.png)

In the above code, we first import the useState hook from the react package. We then define two state variables, result and input, using the useState hook. The result variable will hold the result of the calculations, while the input variable will hold the user input. We then define four event handler functions, handleAdd, handleSubtract, handleMultiply, and handleDivide. These functions will perform the corresponding mathematical operations and update the result variable with the result. We also call the setInput function to reset the input field after each operation. Finally, we return a JSX template that displays an input field for the user to enter input, four buttons for each mathematical operation, and a paragraph that displays the current value of the result variable.

## **Using the Calculator Component**
Now that we have created the Calculator component, let's use it in our App component. Here's the updated code for the App component:
![Alt text](/6.png)

In the above code, we first import the Calculator component from the ./Calculator file. We then include the Calculator component in our JSX template. When we run the application, we should now see the calculator component displayed on the screen.
In the updated code for the App component, we have imported the Calculator component from the Calculator.js file. The App component now simply returns the Calculator component, which will handle all the logic related to the calculator and display the result on the screen.

By using the Calculator component in the App component, we have created a modular and reusable component-based architecture for our calculator application. This approach makes it easy to maintain and extend our code in the future, as we can make changes to individual components without affecting the entire application.

## **Last thoughts about this app**
In this tutorial, we learned how to create a basic maths calculator using React. We first set up the basic structure of our application, then created a Calculator component to handle the calculations and display the result. The useState hook is one of the core features of React that allows us to manage state within our components. By defining state variables with the useState hook, we can easily keep track of changes to the data within our application and trigger updates to the UI as needed.

React also makes it easy to handle user input and respond to events in real-time. We used event handlers and props to pass data between components and trigger updates based on user actions. This was just a basic example, but the concepts and techniques we learned here can be applied to more complex applications.Overall, React provides a powerful and flexible toolset for building dynamic user interfaces that can be easily customized and scaled as needed. Whether you're building a simple calculator or a complex web application, React can help you create engaging and responsive user experiences.

## **Things to keep in mind**
Being New to react There are several things that developers should be aware of and focus on when creating a React app:

 **Component-based architecture:** React is based on the concept of reusable and modular components. Developers should focus on creating small, reusable, and highly cohesive components that can be combined to create complex applications.

 **State management:** In React, state management is a crucial aspect of building applications. Developers should focus on using state management libraries like Redux or MobX to manage state in large applications.

**Performance optimization:** React applications can become slow and unresponsive if not optimized properly. Developers should focus on optimizing their code, reducing the number of re-renders, and using performance tools like the React Profiler to identify performance bottlenecks.

 **Code organization and structure:** As React applications grow in complexity, it becomes important to maintain a clean and organized codebase. Developers should focus on using best practices for code organization and structure, such as separating code into different files, using meaningful variable and function names, and following a consistent code style.

 **Accessibility:** It is important to ensure that React applications are accessible to all users, including those with disabilities. Developers should focus on following accessibility guidelines and using tools like the React Accessibility package to make their applications more accessible.

 **Security:** As with any web application, security should be a top priority when building React applications. Developers should focus on using secure coding practices, validating user input, and using libraries and tools like Helmet and Content Security Policy to protect against common security threats.
