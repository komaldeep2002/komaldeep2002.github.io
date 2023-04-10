---
layout: default
---

<link rel="stylesheet" type="text/css" href="style.css">

# **Reacting To React**
![Alt text](/react-app-1.png)

# **Creating React App**
## **what i have discussed in my last blog**
React JS was developed by Facebook and released as an open-source project in 2013. It has since gained popularity among developers due to its simplicity and scalability. React JS is a popular JavaScript library used for building user interfaces. It is known for its ability to create dynamic and interactive web applications with ease. One of the key benefits of React is its ability to create reusable components, which can save developers time and reduce code duplication. React also has a large and active community, which means there are plenty of resources available for learning and troubleshooting. In addition to building web applications, React can also be used for building mobile applications using frameworks such as React Native. This allows for code reuse between web and mobile applications, making development more efficient. React also has a feature called virtual DOM, which allows for faster rendering of changes to the UI. When a component's state changes, React updates the virtual DOM, which is a lightweight representation of the actual DOM. React then calculates the difference between the old and new virtual DOM and updates the actual DOM only where necessary. React can be used with a variety of other libraries and frameworks, such as Redux for state management and React Router for routing. This makes React a versatile tool for building complex web applications. In this blog post, we will explore the basics of React JS by building a simple maths calculator. We will cover the key concepts of React JS such as components, state, and props, and how they are used to create interactive UI elements. In React, components are the building blocks of UI elements. They are reusable pieces of code that can be used to create complex UIs. Components can be either functional or class components. State is a built-in object in React that allows components to store and manage data. State is used to keep track of the current values of variables that can change over time. When state changes, the component is re-rendered to reflect the new values. Props, short for properties, are used to pass data from a parent component to a child component. Props are read-only and cannot be modified by the child component. Props are used to customize the behavior of a child component and make it more dynamic. To create interactive UI elements in React, you can use state and props to manage the data and functionality of the component. For example, you can create a button component that displays a count and increments the count when clicked.

## **Setting Up the React Environment**
Before we begin, we need to set up the React environment. We will be using Create React App, a tool created by Facebook for setting up a new React project. The first step in setting up the React environment is to install Node.js. Node.js is an open-source, cross-platform, back-end JavaScript runtime environment that executes JavaScript code outside of a web browser. It includes npm, the Node Package Manager, which is used to install and manage third-party packages or libraries that are needed for a project. Once we have Node.js installed, we can use the command line interface (CLI) to run a command that creates a new React project using Create React App. Create React App is a command-line tool that generates a starter kit for a React project. It sets up the development environment with all the necessary configuration files and dependencies pre-installed. Now, we can open our terminal and run the following command:

## **npx create-react-app math-calculator**
The command npx create-react-app math-calculator creates a new React project called "math-calculator" in our current directory. This command will take a few minutes to complete as it downloads all the necessary dependencies and sets up the project files. Once the command finishes, we will have a new folder called "math-calculator" in our directory. Finally, we can open the project in our preferred text editor, such as Visual Studio Code. Visual Studio Code is a free and open-source code editor developed by Microsoft. It has built-in support for JavaScript, React, and many other programming languages and frameworks. Opening the project in our text editor will allow us to start building our math calculator using React.

## **Building the UI Components**
The first step in building our maths calculator is to create the UI components. In React, a component is a reusable piece of code that defines the structure and behavior of a UI element. We will create two components: Display and Keypad. The Display component will display the result of the calculations, and the Keypad component will contain the buttons for performing the calculations. We will start by creating the Display component.

## **Display Component**
We will create a new file called Display.js in the src folder of our project. In this file, we will define the Display component. The code for the Display component is as follows:
![Alt text](/1.png)

In the code above, we have imported the React library and defined a functional component called Display. The Display component takes a prop called result, which is the current result of the calculations. The component returns a div with a class of display, which contains an h2 element that displays the current result.

## **Keypad Component**
Next, we will create the Keypad component. We will create a new file called Keypad.js in the src folder of our project. In this file, we will define the Keypad component. The code for the Keypad component is as follows:
![Alt text](/2.png)

In the code above, we have imported the React library and defined a functional component called Keypad. The Keypad component takes a prop called handleClick, which is a function that handles the button clicks. The component returns a div with a class of keypad, which contains the buttons for performing the calculations.

## **Creating the App Component**
Now that we have created the Display and Keypad components, we can create the App component. The App component will be the parent component that will render the Display and Keypad components. We will create a new file called App.js in the src folder of our project. In this file, we will define the App component. The code for the App component is as follows:
![Alt text](/3.png)

In the code above, we have imported the React library and defined the App component. The App component uses the useState hook to define a state variable called result, which is initially set to an empty string. The component also defines a function called handleClick, which handles the button clicks. The handleClick function checks if the button clicked is the equals sign (=) or the clear button (C). If the button clicked is the equals sign, the function uses the eval() function to evaluate the expression and update the result. If the button clicked is the clear button, the function resets the result to an empty string. If any other button is clicked, the function appends the button to the result. The App component returns a div with a class of app, which contains the title of the calculator, the Display component, and the Keypad component. The handleClick function is passed to the Keypad component as a prop.

## **Styling the Calculator**
Finally, we can add some styles to our calculator to make it look more visually appealing. We will create a new file called App.css in the src folder of our project. In this file, we will define the styles for the calculator. The code for the App.css file is as follows:
![Alt text](/4.png)

## **Creating the Calculator Component**
Now that we have set up the basic structure of our application, let's move on to creating the Calculator component. This component will handle all the logic related to the calculator and display the result on the screen. Here's how we can create the component:
![Alt text](/5.1.png)
![Alt text](/5.2.png)

In the above code, we first import the useState hook from the react package. We then define two state variables, result and input, using the useState hook. The result variable will hold the result of the calculations, while the input variable will hold the user input. We then define four event handler functions, handleAdd, handleSubtract, handleMultiply, and handleDivide. These functions will perform the corresponding mathematical operations and update the result variable with the result. We also call the setInput function to reset the input field after each operation. Finally, we return a JSX template that displays an input field for the user to enter input, four buttons for each mathematical operation, and a paragraph that displays the current value of the result variable.

## **Using the Calculator Component**
Now that we have created the Calculator component, let's use it in our App component. Here's the updated code for the App component:
![Alt text](/6.png)

In the above code, we first import the Calculator component from the ./Calculator file. We then include the Calculator component in our JSX template. When we run the application, we should now see the calculator component displayed on the screen.

## **At Last**
In this tutorial, we learned how to create a basic maths calculator using React. We first set up the basic structure of our application, then created a Calculator component to handle the calculations and display the result. We also learned how to use the useState hook to manage state within our components. This was just a basic example, but the concepts and techniques we learned here can be applied to more complex applications. With React, we can easily build powerful and dynamic user interfaces that respond to user input in real-time.
