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

