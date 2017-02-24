# METEOR-TODO App
![logo](https://upload.wikimedia.org/wikipedia/en/a/a4/Meteor-logo.png "Meteor")

Meteor is a full-stack JavaScript platform for developing modern web and mobile applications. Meteor includes a key set of technologies for building connected-client reactive applications, a build tool, and a curated set of packages from the Node.js and general JavaScript community.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

```
meteor create simple-todos
meteor npm install
meteor npm install --save react react-dom 
meteor npm install --save react-addons-pure-render-mixin
```

### Getting the application running
```
cd simple-todos
meteor npm install
meteor
```
Once you have the above steps completed, open your favorite web browser and type into the web address bar http://localhost:3000 to see the TODO app running. 


### Sample of Component creation

A small code snippet of creating the Task component

> Create App

```
//Meteor allows you to import not only JavaScript in your application, but also CSS and HTML to control load order.
import React, { Component } from 'react';
 
import Task from './Task.jsx';
 
// App component - represents the whole app
export default class App extends Component {
  getTasks() {
    return [
      { _id: 1, text: 'This is task 1' },
      { _id: 2, text: 'This is task 2' },
      { _id: 3, text: 'This is task 3' },
    ];
  }
 
  renderTasks() {
    return this.getTasks().map((task) => (
      <Task key={task._id} task={task} />
    ));
  }
 //The most important method in every React component is render(), which is called by React to get a description of the HTML that this component should display. The HTML content is written using a JavaScript extension called JSX
  render() {
    return (
      <div className="container">
        <header>
          <h1>Todo List</h1>
        </header>
 
        <ul>
          {this.renderTasks()}
        </ul>
      </div>
    );
  }
}
```


### CSS styling

> Cascading Style Sheets (CSS) is a simple mechanism for adding style (e.g., fonts, colors, spacing) to Web documents. Below shows the media CSS for responsive mobile design. 

```
@media (max-width: 600px) {
  li {
    padding: 12px 15px;
  }
 
  .search {
    width: 150px;
    clear: both;
  }
 
  .new-task input {
    padding-bottom: 5px;
  }
```
## Running the app on iOS

> Go to app folder and type:
```
meteor install-sdk ios
```
> Once your are done then type:
```
meteor add-platform ios
meteor run ios
```
## Running on Android

> go to your app folder and type:
```
meteor install-sdk android
```
This will help you install all of the necessary tools to build an Android app from your project. When you are done installing everything, type:
```
meteor add-platform android
```
> After you agree to the license terms, type:
```
meteor run android
```

## Deployment

* [Heroku](https://devcenter.heroku.com/) - Heroku lets you deploy, run and manage applications written in Ruby, Node.js, Java, Python, Clojure, Scala, Go and PHP.


## Built With

* [METEOR](https://www.meteor.com/developers) - Meteor is a full-stack JavaScript platform for developing modern web and mobile applications
* [MongoDB](https://docs.mongodb.com/manual/) - MongoDB is an open-source, document database designed for ease of development and scaling.
 

## Authors

* **Cresta White** - *Contributors* 
* **Alex Diaz** - *Contributors*

## Acknowledgments

* Congrats to the TeamBuddy effort
* GA for all the blood, sweat, and tears.
* Dedication
