# Creating and nesting components

React apps are made out of components. A components is a piece of the UI that has its own logic and appearance. 
A component can be as small as a button, or as large as an entire page.

React components are JavaScript function that return markup.

![image](https://github.com/user-attachments/assets/af1cf1cf-e518-4b48-a5ea-a135240c1538)

in the above image, MyButton start with a capital letter because it is a React Component. React component names must always start with a capital letter, while HTML tags must be lowercase.

The *export default* keywords specify the main component in the file.

**Writing markup with JSX**

JSX is stricter than HTML. you have to close tags like *<br ... />*. Components cannot return multiple JSX tags. You have to wrap them into a shared parent, like a *<div>...</div>* or an empty *<>...</>* wrapper.

![image](https://github.com/user-attachments/assets/4558cbb9-af83-45b1-bf56-fddbc0de6ab1)

**Adding styles**

![image](https://github.com/user-attachments/assets/26c2a325-88fe-4cd8-a471-24a21fbf90fa)

**Displaying Data**

JSX lets you put markup into JavaScript. Curly braces let you "escape back" into JavaScript so that you can embed some variables from your code and display it to the user.

![image](https://github.com/user-attachments/assets/63ea8704-35e2-4fd7-a2b7-e8ed696f9819)

**Conditional rendering**

In React, there is no special syntax for writing conditions. Instead, you'll use the same technique you use when writing regular JavaScript code. 

![image](https://github.com/user-attachments/assets/70673480-c4d8-4f9d-a7e9-20b5577ee568)

**Rendering lists**

Rely on JavaScript features like *for loop* and the *array map() function* to render lists of components.

![image](https://github.com/user-attachments/assets/8fbff0a9-26ab-40a5-b0c6-6237bcc7bee4)

**Responding to events**

You can respond to events by declaring event handler functions inside your components

![image](https://github.com/user-attachments/assets/629608ac-5dd6-4849-b858-a5bd5e4aa37a)


**Updating the screen**

If you want your component to remember to some information and display it:

  1. First import *useState* from 'react';
     
  ![image](https://github.com/user-attachments/assets/7515d074-d230-4d78-8890-e3c7282101c3)

  2. Now you can declare a state variable inside your component

     ![image](https://github.com/user-attachments/assets/e576abe5-5b6b-4314-8db7-07a635d3b301)

You will get 2 things from *useState*: 

  the current state (count) and the function that lets you update it (setCount). You can name them anyhow, but the convention to write is [something, setSomething].

  The first time the button is displayed, count will be 0 because you passed 0 to *useState()*. When you want to change state, call *setCount()* and pass the new value to it.

![image](https://github.com/user-attachments/assets/03ddb966-c424-4d27-ad59-8b90f011835e)

**Using Hooks**

Functions starting with *use* are called Hooks. *useState* is a built-in hook provided by React. Hooks are more restrictive than other functions. You can only call Hooks at the top of your components. If you want to use *useState* in a condition or a loop, extract a new component and put it there.

**Sharing data between components**

To make both button components display the same count and update together, you need to move the state from the individual buttons, upwards to the closest component containing all of them.

![image](https://github.com/user-attachments/assets/0e3e5811-4422-4e10-a41f-e67b5914eb89)

![image](https://github.com/user-attachments/assets/e71f619d-7711-4a42-8a6c-e04f2b78025d)

Then, pass the state from MyApp to each MyButton, together with the shared click handler. Pass info to MyButton using the JSX curly braces

![image](https://github.com/user-attachments/assets/45221c7a-f752-42a8-9321-f508335b82ad)

The info you pass down like this is called props. Now the MyApp component contains the *count* state and the *handleClick* event handler and passes both of them down as props to each of the buttons. Finally, change MyButton to read the props(parameters) you have passed from its parent component:

![image](https://github.com/user-attachments/assets/af46ba58-e176-491d-8234-450173084353)

![image](https://github.com/user-attachments/assets/1dcd65a3-8553-48cf-b3e2-4fbe38346667)
