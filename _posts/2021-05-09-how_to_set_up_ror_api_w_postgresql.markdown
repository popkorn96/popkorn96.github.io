---
layout: post
title:      "How to Set Up RoR API w/ PostgreSQL"
date:       2021-05-10 02:59:50 +0000
permalink:  how_to_set_up_ror_api_w_postgresql
---


The world of backend dev delopment can be difficult to manouver,  but even more so if you are just starting out. Before even starting the Git repository, it's important to consider what relational database managementt system you would want to choose, what relationships your objects are going to have and what kind of data can be manipulated via CRUD. Once you have all of that figured out, you're ready to start you project! <br/><br/>
This post will be about setting up a Ruby on Rails API with a PosgreSQL open source database. Before moving forward, make sure you have installed all necessary programs (i.e Ruby, Rails Gem, PostgreSQL)<br/>

### 1.
To start, make a file in your local drive labeled after the project you would like to create. Its best to keep your different projects in a folder that is accessible and free of clutter that is unrelated to projects.
```
mkdir new-api-app
```
<br/>
Once created, you can ```cd new-api-app``` to navigate into the folder. 
### 2. 
This is when we create our new Ruby on Rails app, readily configured to act as an API with PostreSQL as thne preset database, all. with the help of some very useful flags. The following command typed and executed into the terminal creates a new Rails project directory.
```
rails new basic-api-app --api --database=postgresql
```
### 3. 
Lastly, you can ```cd basic-api-app``` and create a Git repository for your new Rails app. <br/><br/>
This is just the beginning of your app, the real grunt work begins after this as you create your models, controllers and create your database. Getting CRUD implementations on PostreSQL will be featured in the next post, see you there!
