# React

- React is a open-source frontend JavaScript library front-end JavaScript library developed by Facebook in 2011.
- It follows the component based approach which helps in building reusable UI components.
- It is used for developing complex and interactive web and mobile UI.

# Visual Studio Code

- We use Visual Studio Code as Code Editor.
- Install Visual Studio Code -> https://code.visualstudio.com/

# Node.js

- It is a open source run time environment which runs JavaScript code on a server.
- Install Node.js -> https://nodejs.org/en/download/
- To check the node version
```ruby
node -v
```

# npm - Node Package Manager

- It is used to install various dependencies and frameworks on to our project.
- To check the node version
```ruby
npm -v
```

# Babel 

- Whenever we write ES6 code syntax we need Babel which is going to compile ES6 code to ES5 bundles.
- Simply, Babel is a JavaScript compiler.

# Create React App

- Choose the Required Folder
- In Windows, 
```ruby
npm install create-react-app -g
```
- In Mac,
```ruby
sudo npm install create-react-app -g
```
- Finally,
```ruby
create-react-app instawall
```
- where, <b>instawall</b> is the application name

# Elements

```ruby
import React from 'react';
```
- React makes use of Elements to describe the user interface of our Application.
- React Elements are simply objects.
- How to we create React Elements to modify our User Interface.
```ruby
const element = React.createElement('h1', null, 'Hello World');
```
- This element describes the webpage should have a big title(i.e)the big header of Hello World.
- The React elements only describes how the web page looks like but what actually renders our web page is the DOM.
- The process of describing what you want to render and actually rendering the elements is completely de-coupled.
- For that reason we have to import React DOM to be able to required DOM notes from these objects.
```ruby
import ReactDOM from 'react-dom';
```

# Examples 

<b>Example: 1</b>
```ruby
import React from 'react';
import ReactDOM from 'react-dom';

const element = React.createElement('h1', null, 'Hello World');

ReactDOM.render(element, document.getElementById('root'));
```
<b>Example: 2</b>
```ruby
import React from 'react';
import ReactDOM from 'react-dom';

const element = React.createElement('ol', null, 
React.createElement('li', null, 'Android'),
React.createElement('li', null, 'Flutter'),
React.createElement('li', null, 'React')
);

ReactDOM.render(element, document.getElementById('root'));
```
<b>Example: 3</b>
```ruby
import React from "react";
import ReactDOM from "react-dom";

const mArrays = ["Android", "Flutter", "React"];

const element = React.createElement(
  "ol",
  null,
  mArrays.map((mValues, index) => React.createElement("li", { key: index }, mValues))
);

ReactDOM.render(element, document.getElementById("root"));
```

# Understanding JSX

- JSX stands for JavaScript XML. With React, it's an extension for XML-like code for elements and components.
- In Other words, JavaScript extension, or more commonly JSX, is a React extension that allows us to write JavaScript that looks like HTML.
- The JSX is translated to regular JavaScript at runtime.

# Examples

<b>Example: 1</b>
```ruby
import React from "react";
import ReactDOM from "react-dom";

const element = (
  <ol>
    <li>Android</li>
    <li>Flutter</li>
    <li>React</li>
  </ol>
);

ReactDOM.render(element, document.getElementById("root"));
```
