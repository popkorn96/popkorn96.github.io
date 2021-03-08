---
layout: post
title:      "React - Route Render Component"
date:       2021-03-08 01:16:28 +0000
permalink:  react_-_route_render_component
---

React is a framweork that lets you create interactive UI's. You can choose to configure routes if you would prefer not to create a single page application. If you want to go deeper, you are able to consider whether to unmount and mount a new component or simply update a component. While these two lifecycle methods may seem to have an inconsequential influence over how a page is routed to, it has a major effect on your app's performance. Routing is the ability to move between different parts of the application when a user interacts with a page via button, link, image, etc.. Most choose to demonstrate their routes with page tabs or by displaying a menu in which users can decide where to navigate. <br>
A [blog post](http://https://medium.com/the-andela-way/understanding-the-fundamentals-of-routing-in-react-b29f806b157e) by Edmondo Atto describes the **browser router** as the following :
>  The BrowserRouter used for applications which have a dynamic server that knows how to handle any type of URL
>   whereas the HashRouter is used for static websites with a server that only responds
>    to requests for files that it knows about.
>    

<br>
Without diving too deep, a way to implement a browser router and ensure that all of your pages are able to be rendered, follow the steps below =><br>
1. After having initialized your app and created basic components as pages, run the following code to get started with your router congifuration. `npm install react-router-dom
`<br>
2. Import `{ BrowserRouter as Router, Route } from "react-router-dom";` and any components you wish to use as pages as well. 
<br>
3. A React component to render only when the location matches. It will be rendered with route props. it will look like this: <br>
``` ReactDOM.render(
  <Router>
    <Route path="/user" component={User} />
  </Router>); ```
<br>
4. The final route render component will look like so:<br>

```import React from "react";
import ReactDOM from "react-dom";
import { BrowserRouter as Router, Route } from "react-router-dom";
import User from "./User.js"
ReactDOM.render(
<Router>
<Route path="/user component={User}">
<Router>
);
```
<br>
And there you have your component based react router, you can add as many routes and components in tandem as you would like, but it is not recommended to have more than necessary as React is based of the principle of reusable components. 

