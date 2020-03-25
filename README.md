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
- Whenever we are writting JSX, as a rule of them every thing must quote to a single JSX element.

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
<b>Example: 2</b>
```ruby
import React from "react";
import ReactDOM from "react-dom";

const mArrays = ["Android", "Flutter", "React"];

const element = (
  <ol>
    <li>{mArrays[0]}</li>
    <li>{mArrays[1]}</li>
    <li>{mArrays[2]}</li>
  </ol>
);

ReactDOM.render(element, document.getElementById("root"));
```
<b>Example: 3</b>
```ruby
import React from "react";
import ReactDOM from "react-dom";

const mArrays = ["Android", "Flutter", "React"];

const element = (
  <ol>
    {mArrays.map((mValues, mIndex) => (
      <li key = {mIndex}>{mValues}</li>
    ))}
  </ol>
);

ReactDOM.render(element, document.getElementById("root"));
```

<b>Example: 4</b>
```ruby
import React from "react";
import ReactDOM from "react-dom";

const mArrays = ["Android", "Flutter", "React"];

const element = (
  <div>
    <h1>Title</h1>
    <ol>
      {mArrays.map((mValues, mIndex) => (
        <li key={mIndex}>{mValues}</li>
      ))}
    </ol>
  </div>
);

ReactDOM.render(element, document.getElementById("root"));
```

# Components

 - Compoenents are the main building blocks of an Application.
 - You can see a UI broken down into multiple individual pieces called components and work on them independently and merge them all in a parent component which will be your final UI.
 
# Examples

<b>Example: 1</b>
```ruby
import React, { Component } from "react";
import ReactDOM from "react-dom";

const mArrays = ["Android", "Flutter", "React"];

class Title extends Component {

  render() {
    return (
      <h1>Title</h1>
    );
  }

}

class List extends Component {

  render() {
    return (
      <ol>
        {mArrays.map((mValues, mIndex) => (
          <li key={mIndex}>{mValues}</li>
        ))}
      </ol>
    );

  }

}

class Main extends Component {
  render() {
    return (
      <div>
        <Title />
        <List />
      </div>
    )
  }
}

ReactDOM.render(<Main />, document.getElementById("root"));
```
<b>Example: 1</b>
```ruby
import React, { Component } from "react";
import ReactDOM from "react-dom";


class Title extends Component {

  render() {
    return (
      <h1>{this.props.mString}</h1>
    );
  }

}

class List extends Component {

  render() {
    return (
      <ol>
        {this.props.mArrays.map((mValues, mIndex) => (
          <li key={mIndex}>{mValues}</li>
        ))}
      </ol>
    );

  }

}

class Main extends Component {
  render() {
    return (
      <div>
        <Title mString={'Title'} />
        <List mArrays={["Android", "Flutter", "React"]} />
        <List mArrays={["React", "Flutter", "Android"]} />
      </div>
    )
  }
}

ReactDOM.render(<Main />, document.getElementById("root"));
```

# Refractor

<b>Example: 1</b>

- Create the Folder as Components
- Create the File name as Main.js, Title.js and List.js in the above mentioned Folder.

__In Main.js__
```ruby
import React, { Component } from "react";
import Title from "./Title";
import List from "./List"

class Main extends Component {
  render() {
    return (
      <div>
        <Title mString={"Title"} />
        <List mArrays={["Android", "Flutter", "React"]} />
        <List mArrays={["React", "Flutter", "Android"]} />
      </div>
    );
  }
}

export default Main;
```

__In Title.js__
```ruby
import React, { Component } from "react";

class Title extends Component {

    render() {
        return (
            <h1>{this.props.mString}</h1>
        );
    }

}

export default Title;
```

__In List.js__
```ruby
import React, { Component } from "react";

class List extends Component {
  render() {
    return (
      <ol>
        {this.props.mArrays.map((mValues, mIndex) => (
          <li key={mIndex}>{mValues}</li>
        ))}
      </ol>
    );
  }
}

export default List;
```

__In index.js__
```ruby
import React from "react";
import ReactDOM from "react-dom";
import Main from "./Components/Main";

ReactDOM.render(<Main />, document.getElementById("root"));
```

# State Management

- React components has a built-in state object.
- The state object is where you store property values that belongs to the component.
- When the state object changes, the component re-renders.
- The set state property allows us to update this special state property here and it will then ensure that React gets to know about this update and updates the DOM.
- set state takes an object as an argument and it will merge whatever we define here with our existing state.

# Prop - Types

```ruby
npm install --save prop-types
```
