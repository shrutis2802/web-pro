Header Component
The Header component is a simple navigation bar designed for use in a React web application. It displays a list of navigation items and highlights the active item. The header supports theming (light and dark) and includes a flexible layout.

Features
Dynamic Navigation: The navigation items are generated dynamically from an array of objects.
Active Tab Highlighting: The active tab is highlighted with a different background color and text color.
Theming Support: The header style changes based on the current theme (light or dark).
Responsive Design: The layout is flexible and adapts to different screen sizes.
Installation
To use this component in your React application, follow these steps:

Install React (if you haven't already):

bash
Copy
npx create-react-app my-app
cd my-app
Create the Header component: Create a file Header.js in the src folder of your React project and paste the Header component code into it.

Import and use the Header component in your main App.js file:

jsx
Copy
import React, { useState } from 'react';
import Header from './Header';  // Import the Header component

function App() {
  const [activeTab, setActiveTab] = useState("home");
  const [theme, setTheme] = useState("light");  // You can toggle between "light" and "dark" themes

  return (
    <div>
      <Header activeTab={activeTab} setActiveTab={setActiveTab} theme={theme} />
      {/* Your other components go here */}
    </div>
  );
}

export default App;
Styling: You can customize the styles further by modifying the headerStyle, navStyle, or adding your own CSS classes.

Props
activeTab (string)
Type: string
Description: The ID of the currently active tab.
Example: "home", "about", "todo", "profile", "counter"
setActiveTab (function)
Type: function
Description: A function to update the active tab state.
Example:
jsx
Copy
const [activeTab, setActiveTab] = useState("home");
theme (string)
Type: string
Description: The theme of the header. It supports two values: "light" and "dark".
Example: "light", "dark"
Example Usage
jsx
Copy
import React, { useState } from 'react';
import Header from './Header';

function App() {
  const [activeTab, setActiveTab] = useState("home");
  const [theme, setTheme] = useState("light");

  return (
    <div>
      <Header activeTab={activeTab} setActiveTab={setActiveTab} theme={theme} />
      {/* Other components */}
    </div>
  );
}

export default App;
Customization
You can customize the navItems array to add more navigation items or change the text/ID of existing items.
Modify the headerStyle and navStyle objects to change the appearance of the header.
Add more functionality, such as a theme toggle button or a logo, by expanding the component.
License
This project is open-source and available under the MIT License.

