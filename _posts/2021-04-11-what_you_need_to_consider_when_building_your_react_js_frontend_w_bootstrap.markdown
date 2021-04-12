---
layout: post
title:      "What You Need To Consider When Building Your React.js Frontend w Bootstrap"
date:       2021-04-12 03:40:10 +0000
permalink:  what_you_need_to_consider_when_building_your_react_js_frontend_w_bootstrap
---


As far as Frontend Development goes, React has been such an easy tool to use. Reusable components and a declarative style is something I've become very familiar with in the past months. The project I had volunteered for recently has to do with a single user webpage with OAUTH, Google Authenticator, and Bootstrap for styling. It has been a fun week and below I'll describe a few details to consider that I think would be beneficial for any basic React.js app to use that would be simple to make with react-bootstrap!

#### Pages
For each page you create, it would be wise to consider creating a container. You do not have to have a component make up the entirety of each page, but it could encapsulate all of the other components you would want each page to include. 
For example, your home page could include your page's notification box or the website footer. React's reusable components allow for so much flexibility so, should you decide to move any of these around you can most definitely do so.

#### Routes
For each page you create, you are encouraged to create a route. Your routes can be encapsulated in your App component, through which you can allow for different routes to be allowed, depending on a user's session status, should you choose to include a user aspect to your site. 

#### Users
If you decide to have multiple users, make your own API in which you can encrypt your user's login information. Having something to stand between your site and hackers will make your users appreciate your attention to their privacy and you might even get more visits! There are also external login options you can use such as OAuth or Google Authenticator that can make your site that much more inclusive. 

#### Navbar
The first thing to consider when creating the Frontend of a website I think should be the Navbar. Of course, this would have to be after having had considered and created all of the above. The navbar is the main navigational panel that your users would refer to when moving about your page. They should include somewhere to be able to navigate to your home page, login (login/logout applicable), and other main pages you want your users to be easily able to access. 

#### React-Bootstrap
The best way to consume React-Bootstrap is via the npm package which you can install with npm.
```
npm install react-bootstrap bootstrap
```
<br/>
If you are importing a single component, you are able to do so like this:
```
import Button from 'react-bootstrap/Button';
```
<br/>
If you are importing multiple components from bootstrap, you are able to do it like this:<br/>
```
import { Button } from 'react-bootstrap';
```
### Conclusion
There are so many different components that react-bootstrap offers and I have a lot of fun tinkering and updating my CSS to make it JUST the way I want my Frontend to be. Give it a shot and you'll see just how simple and fun it can really be!

