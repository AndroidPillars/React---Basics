# React.js

:point_right: Click :star: if you like the project.   
:point_right: Pull Request are highly appreciated.  
:point_right: Follow me [@Gowtham R](https://twitter.com/Gowtham26730226) for new technical updates.  

## Topics

| S.No | Content |
| --------	 | ------------ |
| 1 | [React](README.md#react) |
| 2 | [Virtual DOM](README.md#virtual-dom) |
| 3 | [Visual Studio Code](README.md#visual-studio-code) |
| 4 | [Node.js](README.md#nodejs) |
| 5 | [npm - Node Package Manager](README.md#npm---node-package-manager) |
| 6 | [JavaScript - ES6](README.md#javascript---es6) |
| 7 | [var and let](README.md#var-and-let) |
| 8 | [var vs let](README.md#var-vs-let) |
| 9 | [const](README.md#const) |
| 10 | [Arrow Functions](README.md#arrow-functions) |
| 11 | [Template String](README.md#template-string) |
| 12 | [Function Parameters](README.md#function-parameters) |
| 13 | [ES6 - Classes](README.md#es6---classes) |
| 14 | [Spread Operator](README.md#spread-operator) |
| 15 | [Babel](README.md#babel) |
| 16 | [Create React App](README.md#create-react-app) |
| 17 | [Elements](README.md#elements) |
| 18 | [Understanding JSX](README.md#understanding-jsx) |
| 19 | [Components](README.md#components) |
| 20 | [Refractor](README.md#refractor) |
| 21 | [Setting Styles](README.md#setting-styles) |
| 22 | [Functional Components](README.md#functional-components) |
| 23 | [Class Components](README.md#class-components) |
| 24 | [Props](README.md#props) |
| 25 | [State Management](README.md#state-management) |
| 26 | [Prop - Types](README.md#prop---types) |
| 27 | [React State Management Lifecycle Methods](README.md#react-state-management-lifecycle-methods) |
| 28 | [Tools Reference](README.md#tools-reference) |


## React

- React is a open-source frontend JavaScript library front-end JavaScript library developed by Facebook in 2011.
- It follows the component based approach which helps in building reusable UI components.
- It is used for developing complex and interactive web and mobile UI.  
&nbsp;  
  <b>For Example</b>  
  &nbsp;
  ```ruby
  webpage
   <searchBar/>
   <blogPost/>
  webpage
  ```
  - <b>where</b>, the webpage component is made up of two sub components.
  - searchBar and blogPost components combine together to form the entire webpgae.
  - This is known as compositional model.
  - React is just JavaScript.
  
## Virtual DOM

- The Components we just talked above is made up of Elements.
- These Elements describes the UI of our webpage.
- With the help of Virtual DOM React takes care of all the hard work of converting the elements that we created through DOM   Nodes which are passed on to the actual DOM and renders appropriate UI on our webpage.

## Visual Studio Code

- We use Visual Studio Code as Code Editor.
- Install Visual Studio Code -> https://code.visualstudio.com/

## Node.js

- It is a open source run time environment which runs JavaScript code on a server.
- Install Node.js -> https://nodejs.org/en/download/
- To check the node version  
  &nbsp;
  ```ruby
  node -v
  ```

## npm - Node Package Manager

- It is used to install various dependencies and frameworks on to our project.
- To check the node version  
  &nbsp;
  ```ruby
  npm -v
  ```

## JavaScript - ES6

## var and let 

- <b>let</b> is an update that came along with ES6.
- <b>Var</b> defines variables that can be reassigned.

  <b>For Example</b>,
  
  ```ruby
  var name = "Android";
  console.log(name);
  name = "Flutter";
  console.log(name);
  ```
- In Var you cannot access the variable outside the scope(i.e) when you declare a variable in var it is scoped to the enclosing function.
- var is a function scoped.

  <b>For Example</b>,

  ```ruby
  function printName(){
    var name = "Android";
    console.log(name);
  }
  console.log(name); // Outside the Scope it will thorugh an error
  printName();
  ```
- To understand why ES6 is updated, let is a not a function scoped it is block scoped.

  <b>For Example</b>,
  
  ```ruby
  var name = "Android";
  
  if(name == "Android"){
    let myName = " Flutter";
    console.log(myName);
    }
    console.log(myName); // Outside the Scope it will thorugh an error
  ```
  
## var vs let

- In var, we can reuse the variable names.

## var

  <b>For Example</b>,

  ```ruby
   var age = 20;
   var age = 22;
   console.log(age);
  ```
  
## let

  <b>For Example</b>,

  ```ruby
   var age = 20;
   age = 22;
   console.log(age);
  ```
  
## const 

- In const Once you assign a value, you cannot update that again.

  <b>Example 1</b>,
  
  ```ruby
  const age = 20;
  console.log(age);
  ```
 - The below Example throws an Exception because we are trying to reassign the person var, 
  
    <b>Example 2</b>,
  
    ```ruby
    const person = {
    name: 'Android';
    company: 'google';
    }
 
    person = {
    name: 'Windows';
    company: 'Microsoft';
    }
 
    console.log(person.name);
    console.log(person.company);
    ```
 
- In const, we will never allow to change the value of an object but we can change it's properties.

  <b>Example 3</b>,
  
  ```ruby
  const person = {
  name: 'Android';
  company: 'google';
  }
 
  person.name: 'Windows';  
  person.company: 'Microsoft';
 
  console.log(person.name);
  console.log(person.company);
  ```
  
## Arrow Functions

<b>In ES5</b>,
```ruby
const integers = [1,2,3];

const updatedIntegers = integers.map(function(number) {
  return number += 1;
}

console.log(updatedIntegers);
```

<b>ES6 Arrow Functions</b>,
```ruby
const integers = [1,2,3];

const updatedIntegers = integers.map((number) => {
  return number += 1;
}

console.log(updatedIntegers);
```

```ruby
const integers = [1,2,3];

const updatedIntegers = integers.map((number) => number += 1);

console.log(updatedIntegers);
```

```ruby
const integers = [1,2,3];

const updatedIntegers = integers.map(number => number += 1);

console.log(updatedIntegers);
```

```ruby
const integers = [1,2,3];

const updatedIntegers = integers.map(() => "bob");

console.log(updatedIntegers);
```

<b>Using Filter</b>,

```ruby
const ages = [23, 24, 3, 19];

const adults = ages.filter(function(age){
  return age > 20;
});

console.log(adults);
```

```ruby
const ages = [23, 24, 3, 19];

const adults = ages.filter((age) => age > 20);

console.log(adults);
```

## Template String 

<b>In ES5</b>,
```ruby
const name = 'Android';
const age = 25;

const mDescription = 'My name is ' + name + ', and I am ' + age + ' years old';

console.log(mDescription);
```

<b>In ES6</b>,
```ruby
const name = 'Android';
const age = 25;

const mDescription = `My name is ${name}, and I am ${age * 2} years old`;

console.log(mDescription);
```

## Function Parameters

## Objects  
- An object is nothing but a self-contained component which consists of methods and properties to make a particular type of data useful. 
- Object determines the behavior of the class.

  ```ruby
  const person = {
  name: 'Android',
  age: 8
  }
  console.log(person);
  ```
  
## Function Constructor

```ruby
function Person(name, age) {
  this.name = name;
  this.age = age;
}

const bill = new Person('Android',50);
console.log(bill);
```

```ruby
function Person(name, age) {
  this.name = name;
  this.age = age;
}

const bill = new Person('Android',50);
console.log(bill);
```

```ruby
function Person(name, age) {
  this.name = name;
  this.age = age;
}

Person.prototype.speak = function(){
  console.log(`Hi my name is $(this.name}`);

};

const bill = new Person('Android',50);
bill.speak();
```

## ES6 - Classes

```ruby
class Person{

constructor(){
  this.name = name;
  this.age = age;
}

const bill = new Person('Android',50);
console.log(bill);
}
```

```ruby
class Person{

constructor(){
  this.name = name;
  this.age = age;
}

speak(){
  console.log(`Hi my name is $(this.name}`);
}

const bill = new Person('Android',50);
bill.speak();
}
```

```ruby
class Person{

constructor(){
  this.name = name;
  this.age = age;
  this.children = children;
}

speak(){
  console.log(`Hi my name is $(this.name}`);
}

birth(child){
  this.children.push(child);
}

const bill = new Person('Android', 50, ['Android', 'Flutter']);
bill.speak();
bill.birth('React');
console.log(bill.children);
}
```

## Spread Operator

```ruby
const names = ['Android', 'Flutter', 'React']
const moreNames = ['Google', 'Microsoft']

console.log(names)
```

```ruby
const names = ['Android', 'Flutter', 'React']
const moreNames = ['Google', 'Microsoft']

console.log(...names) 
```

```ruby
const names = ['Android', 'Flutter', 'React']
const moreNames = ['Google', 'Microsoft']

let allNames = []
allNames = allNames.concat(names)
allNames.push('Flipkart')
allNames = allNames.concat(moreNames)

console.log(allNames)
```

```ruby
const names = ['Android', 'Flutter', 'React']
const moreNames = ['Google', 'Microsoft']

const allNames = [...names, 'Gio', ...moreNames]

console.log(allNames)
```

## Babel 

- Whenever we write ES6 code syntax we need Babel which is going to compile ES6 code to ES5 bundles.
- Simply, Babel is a JavaScript compiler.

## Create React App

- Choose the Required Folder
- In Windows,  
  &nbsp;  
  ```ruby
  npm install create-react-app -g
  ```
- In Mac,  
  &nbsp;  
  ```ruby
  sudo npm install create-react-app -g
  ```
- Choose the Destination Folder.
- Finally,  
  &nbsp;  
  ```ruby
  create-react-app instawall
  ```
- where, <b>instawall</b> is the application name
- Now Open the Application Folder using Visual Studio Code.

# Elements

- React makes use of Elements to describe the user interface of our Application.  
  &nbsp;  
  ```ruby
  import React from 'react';
  ```
- React Elements are simply objects.
- How to we create React Elements to modify our User Interface.  
  &nbsp;  
  ```ruby
  const element = React.createElement('h1', null, 'Hello World');
  ```
- This element describes the webpage should have a big title(i.e)the big header of Hello World.
- The React elements only describes how the web page looks like but what actually renders our web page is the DOM.
- The process of describing what you want to render and actually rendering the elements is completely de-coupled.
- For that reason we have to import React DOM to be able to required DOM notes from these objects.  
  &nbsp;  
  ```ruby
  import ReactDOM from 'react-dom';
  ```
- <b>Note</b>: You can check the libraries installation in package.json file -> dependencies.

## Examples 

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

## Understanding JSX

- JSX stands for JavaScript XML. With React, it's an extension for XML-like code for elements and components.
- In Other words, JavaScript extension, or more commonly JSX, is a React extension that allows us to write JavaScript that looks like HTML.
- The JSX is translated to regular JavaScript at runtime.
- Whenever we are writting JSX, as a rule of them every thing must quote to a single JSX element.

## Examples

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

<b>Example: 5 (Using javascript)</b>
```ruby
import React from "react";
import ReactDOM from "react-dom";

const h1 = React.createElement("h1", null, "Header");
const p = React.createElement("p", null, "Description");
const myElement = React.createElement("div", null, h1, p);

ReactDOM.render(myElement, document.getElementById("root"));
```  

<b>Example: 6</b>
```ruby
import React from "react";
import ReactDOM from "react-dom";

function One() {
  return <h1>Hello</h1>;
}

ReactDOM.render(<One/>, document.getElementById("root"));

```  

## Components

 - Compoenents are the main building blocks of an Application.
 - You can see a UI broken down into multiple individual pieces called components and work on them independently and merge them all in a parent component which will be your final UI.
 
## Examples

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
<b>Example: 2</b>
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
- <b>this</b> keyword points out to the component instance of the class that is being rendered.

## Refractor

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

## Setting Styles 

- To install font from online sources,

  <b>In stylesheet.css</b>,
  
  ```ruby
    @font-face {
      font-family: 'billabong';
      src: url("https://cdn.rawgit.com/milktronics/beaglegr.am/master/public/fonts/billabong-webfont.woff");
    }
  ``` 
  
- Some of the font properties for heading is given below,
 
  <b>In stylesheet.css</b>,
  
  ```ruby
  h1 {
    font-family:  'billabong';
    text-align: center;
    font-size: 13rem;
    font-weight:100;
    margin: 2rem 0;
    letter-spacing: -1px;
    color : black;
  } 
  ```
## Functional Components

- Functional components are simply javascript functions.
- We can create a functional component in React by writing a javascript function.
- These functions may or may not receive data as parameters.  
  &nbsp;  
  ```ruby
  function Demo() {
  
    return <h1>Welcome Message!</h1>;
    
  }
  ```
  
## Examples 

<b>Example: 1</b>
```ruby
import React from "react";
import ReactDOM from "react-dom";

function Header() {
  return <h1>Header</h1>;
}

function Body() {
  return <h1>Decription</h1>;
}

function Footer() {
  return <h1>Footer</h1>;
}
ReactDOM.render([<Header/>, <Body/>, <Footer/>], document.getElementById("root"));

```  

<b>Example: 2</b>
```ruby
import React from "react";
import ReactDOM from "react-dom";

function Header() {
  return <h1>Header</h1>;
}

function Body() {
  return <h1>Decription</h1>;
}

function Footer() {
  return <h1>Footer</h1>;
}

function Layout() {
  return (
    <div>
    <Header />
    <Body/>
    <Footer/>
    </div>
  )
}
ReactDOM.render( <Layout/>, document.getElementById("root"));
```  

<b>Example: 3</b>

   __In App.js__  
    
    ```ruby  
    import React from "react";
    import ReactDOM from "react-dom";
    import Demo from './Demo'

    ReactDOM.render( <Demo/>, document.getElementById("root"));

    ```  
    
   __In Demo.js__  
    
   ```ruby
   import React from 'react';

    function Demo(props){
      return(
        <p1>Description {props.name}</p1>
      )
    }

   export default Demo;
   ```


## Class Components

- The class components are little more complex than the functional components.
- The functional components are not aware about the other components in your program where as the class components can work   with each other.
- We can pass data from one class component to other class component.
- We can use javascript ES6 classes to create class based components in React.
  
  ```ruby
  class Demo extends React.Component {
 
    render(){
          return <h1>Welcome Message!</h1>;
    }
    
  }
  ```  
  
## Examples 

<b>Example: 1</b>

   __In App.js__  
    
    ```ruby  
    import React from "react";
    import ReactDOM from "react-dom";
    import Demo from './Demo'

    ReactDOM.render( <Demo/>, document.getElementById("root"));

    ```  
    
   __In Demo.js__  
    
   ```ruby
   import React,{Component} from 'react';

   class Demo extends Component
    {
      render(){
        return(
          <p1>Description</p1>
        )
      }
    }

   export default Demo;
   ```


## Props

- Props are arguments passed into React components.
- Props are passed to components via HTML attributes.
- Props are considered to be read only immutable data it can't be changed overtime.

## Examples 

  <b>Example: 1</b>

   __In App.js__  
    
   ```ruby  
   import React from "react";
   import ReactDOM from "react-dom";
   import Demo from './Demo'

   ReactDOM.render(<Demo name = {"by AndroidPillars"}/>, document.getElementById("root"));

   ```  
    
   __In Demo.js__  
    
   ```ruby
   import React,{Component} from 'react';

   class Demo extends Component
    {
      render(){
        return(
          <p1>Description {this.props.name}</p1>
        )
      }
    }

   export default Demo;
   ```

## State Management

- React components has a built-in state object.
- The state object is where you store property values that belongs to the component.
- When the state object changes, the component re-renders.
- The set state property allows us to update this special state property here and it will then ensure that React gets to know about this update and updates the DOM.
- set state takes an object as an argument and it will merge whatever we define here with our existing state.  
  &nbsp;  
  ```ruby
  class Demo extends React.Component {  
      
    constructor(){  
        super();  
        this.state = {  
            message: "my friend (from state)!"  
        };  
    }  
      
    render() {  
        return <h1>Hello {this.state.message}!</h1>;  
    }  
  }
  ```  
  
## Examples 

  <b>Example: 1</b>

   __In App.js__  
    
   ```ruby  
   import React from "react";
   import ReactDOM from "react-dom";
   import Demo from './Demo'

   ReactDOM.render(<Demo mValue = {"by AndroidPillars"}/>, document.getElementById("root"));

   ```  
    
   __In Demo.js__  
    
   ```ruby
   import React,{Component} from 'react';

    class Demo extends Component
    {

      constructor(){
      super();
      this.state = {
          name: "AndroidPillars"
      }
    }

    render(){
      const {name} = this.state
      return(
        <p1>Description {name}</p1>
      )
    }
  }


  export default Demo;
  ```


## Prop - Types

- We can use the propType for validating any data we are receiving from props. 

  ```ruby
  npm install --save prop-types
  ```

## React State Management Lifecycle Methods

- The constructor is only used to initialize the state of our Component or bind methods to the proper context.
- The componentDidMount method is invoked immediately after the component is being inserted in to the DOM.
- <b>Flow by using componentDidMount method</b>, Constructor -> No Elements -> Render -> ComponentDidMount ->         ApiRequest -> UpdateState -> Re-render(i.e)Render.
- The componentWillMount method as is called as the constructor(i.e) before the component is invoked in to the         DOM(i.e)before the render method gets invoked.
- The componentDidUpdate method gets called once the component is Re-rendered(i.e) whenever we update the state of our Component trigger a Re-render.

## React - Router

- We will be using React Router in to a Single Page Application.
- In <b>Single Page Application,</b> it downloads the entire content in a Single Request.(i.e) A single-page application       works inside a browser and does not require page reloading during use.
- We split React Router in to three components.  
  1. Browser Router
  2. Link
  3. Route
  
- We have to connect our Browser Router to a link component. Since it is the link component on which the   user will press that tells the browser router to update the URL for helping our app to listen URL changes     which renders to the right screen.
  
<b>For Installing the Plugin,</b>
```ruby
npm install react-router-dom
```
  
## Browser Router

- Browser Component is used to keep track of URL changes.  
&nbsp;  
  ```ruby
  import {BrowserRouter} from 'react-router-dom'
  
  ReactDOM.render(<BrowserRouter><App/></BrowserRouter>, document.getElementById('root'));
  ```

## Link

- Link Component is used to invoke a change in the URL upon it is being clicked on(ie)it's similar to that of the hyper link.  
  &nbsp;  
  ```ruby
  import {Link} from 'react-router-dom'
  
  <Link className="add-icon" to="/add-photo"></Link>
  ```

## Route

- Based on the URL we are going to have Route which contains the given path, whatever the URL are directed by the Link Component are going to find the proper Route which has the given path associated with the link.  
  &nbsp;  
  ```ruby
  import {Route} from 'react-router-dom';
  
  <Route path="/..." component = {...}/>
  
  ```

## Redux

- Redux makes our state of the Application more Predictable. 
- As our application becomes more complex(i.e) whenever you miss manage the state as a result your are exposed to a lot of Bugs that's what the redux is the good alternative to managing our application state.
- It makes the thing light Easier.
- Redux gives us the way to store our data in a Organised way. All of our app's data is centralised in a single <b>Store</b>.
- Next, State in Redux is Read only, the component cannot never directly change the State it can do only by <b>Action</b>.
- All State changes in a redux is happen in a single place that's what we mentioned Redux makes our state of the Application more Predictable, Easier to keep track of and easier to debug.
- All State is updated one by one in a very strict order.
- The Root Reducer is the only thing that updates the State.  
  &nbsp;  
  <b>For Installing Redux Framework,</b>     
  &nbsp;  
  ```ruby
  npm install redux
  ```
- Finally, Redux has the ability to keep the state predictable, Easy to Manage such that it's centralized in a single store   only pure functions called Reducers allow to update the State.
- The three main parts in Redux are <b>Store, Reducer</b> and <b>Action</b>.
- <b>Store</b> where our application state lives. All the data in application lives in the Store.
- State in Redux is read-only. It's immutable.
- The only way to change the State that lives inside our Store is through the pure functions called <b>reducers</b>.
- <b>Reducer</b> is the arguement which we pass in to the createStore. The arguement takes in to the bunch of reducers which    all combine in to a single root reducer which will define how data is going to be updated in our Store.  
    &nbsp;  
    ```ruby
    import { createStore } from 'redux'
    import rootReducer from './redux/reducer'
  
    const store = createStore(rootReducer)
    
    ReactDOM.render(<BrowserRouter><App/></BrowserRouter>, 
    document.getElementById('root'));

    ```
    __In reducer.js__  
    &nbsp;  
    ```ruby
    const postReducer = function posts(state , action) {
      return state
    }
    
    export default postReducer
    ```
- The Store dispatches an Action and the Action disptaches to the Reducer and the Reducer then gives the Store with its       updated State.   
    &nbsp;  
    <b>For Installing React-Redux,</b>   
    &nbsp;  
    ```ruby
    npm install react-redux
    ```
- By Installing react-redux it gives access to the provider.
- The provider provide our Store to it's child Component.  
  &nbsp;  
    ```ruby
    import { createStore } from 'redux'
    import rootReducer from './redux/reducer'
    import {provider} from 'react-redux'
    import App from './Components/App'
  
    const store = createStore(rootReducer)
    
    ReactDOM.render(<Provider store = {store}><BrowserRouter><App/></BrowserRouter></Provider>, 
    document.getElementById('root'));

    ```
    __In App.js__  
    &nbsp;  
    ```ruby
    import Main fron './Main'
    import {connect} from 'react-redux'
    
    function mapStateToProps(state) {
      return {
        posts: state
      }
    }
    
    const App = connect(mapStateToProps)(Main)
    
    export default App
    ```
    __In Action.js__  
    &nbsp;  
    ```ruby
    export function removePost(index) {
      return {
        type: 'REMOVE_POST',
        index: index
      }
    }
    ```
- By Using React Developer Tools(i.e) Chrome -> Extension -> React Developer Tools -> https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi/related -> By Clicking “>>” -> you will find “Components” and “Profiler”.

## FireBase

- Firebase is a technology that allows you to create web and mobile applications without server-side programming, making development faster and easier. 
- Visit, https://console.firebase.google.com/u/0/
- Create a project.
- Now Create a new Database and select the Option Realtime Database.
- Now, Go to the Database and make the read and write value as true for disabling the Authentication.
- Go to Project Overview and select Add Firebase to your web app.
- Once you created, Go to settings and copy the config,  
  &nbsp;  
  ```ruby
    const firebaseConfig = {
    apiKey: "AIzaSyDcsxmF3vVIgcQ30DR-D6dgyo24qde",
    authDomain: "photowall-6cd25.firebaseapp.com",
    databaseURL: "https://photowall-6cd25.firebaseio.com",
    projectId: "photowall-6cd25",
    storageBucket: "photowall-6cd25.appspot.com",
    messagingSenderId: "308221131146",
    };
  ```
  <b>For Installing Firebase</b>   
    &nbsp;  
    ```ruby
      npm install firebase
    ```  
    
# Tools Reference

- https://codesandbox.io/ (online Editor)
