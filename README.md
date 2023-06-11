# Styled-Component

React Styled Components - Student Guide
Welcome to the React Styled Components Student Guide! This document will provide you with a brief introduction to using Styled Components in your React projects.

Table of Contents
What are Styled Components?
Installation
Usage
Creating Styled Components
Passing Props
Global Styles
Themes
Conclusion
What are Styled Components?
Styled Components is a library for styling React components using tagged template literals. It allows you to write CSS code within your JavaScript files, making it easy to create and manage component-specific styles. Styled Components promotes a modular and reusable approach to styling, improving code maintainability and reducing style-related conflicts.

Installation
To use Styled Components in your React project, you need to install it first. Open your project's terminal and run the following command:

bash
Copy code
npm install styled-components
or if you are using Yarn:

bash
Copy code
yarn add styled-components
Usage
Once you have installed Styled Components, you can import it into your React components and start using it.

javascript
Copy code
import styled from 'styled-components';
Creating Styled Components
Styled Components allows you to define custom styles for your React components. You can create a styled component by calling the styled function and passing a valid HTML element or a component as the argument.

javascript
Copy code
const Button = styled.button`
  background-color: #007bff;
  color: white;
  padding: 8px 16px;
  border: none;
  border-radius: 4px;
  cursor: pointer;

  &:hover {
    background-color: #0056b3;
  }
`;
In the example above, we create a styled button component with custom styles. The styles are defined using CSS syntax within the template literal. You can include any valid CSS rules and properties.

Passing Props
Styled Components allows you to pass props to your styled components and conditionally apply styles based on those props. To access the props within the styles, you can use a function instead of a template literal.

javascript
Copy code
const Alert = styled.div`
  background-color: ${(props) => props.variant === 'success' ? 'green' : 'red'};
  color: white;
  padding: 16px;
`;
In the example above, we create an alert component that changes its background color based on the variant prop. If the variant prop is set to 'success', the background color will be green; otherwise, it will be red.

Global Styles
Styled Components also allows you to define global styles that will be applied to your entire application. To create global styles, you can use the createGlobalStyle function.

javascript
Copy code
import { createGlobalStyle } from 'styled-components';

const GlobalStyles = createGlobalStyle`
  body {
    font-family: Arial, sans-serif;
  }
`;
In the example above, we define a global style for the body element, setting the font-family to Arial.

Themes
Styled Components supports theming, allowing you to define different sets of styles based on a theme object. This can be useful for creating light and dark themes or customizing the appearance of your components based on different contexts.

javascript
Copy code
import { ThemeProvider } from 'styled-components';

const theme = {
  colors: {
    primary: 'blue',
    secondary: 'red',
  },
};

function App() {
  return (
  )
}