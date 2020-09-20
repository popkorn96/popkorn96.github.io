---
layout: post
title:      "Sinatra Project"
date:       2020-09-20 18:06:07 -0400
permalink:  sinatra_project
---

 <strong>SINATRA!</strong> A library built in Ruby - for Ruby. This neat gem lets us program on Ruby much easier than without. Building this project from scratch was much more rewarding than the first project we did at Flatiron. I was able to work more closely with HTML formatting and CSS styling. The example webapp that is used to confirm that corneal was successfully installed and is functioning correctly also gave me a look inside its web design with HTML and CSS. <br>
I decided to go with a Bills App for this project becuase I do see organization as a great tool that could be used by anyone, likewise I wanted to make it user friendly. I got started by doing the following:<br><br>
<ol>
<li>Install Corneal gem</li>
<li>Use 'corneal scaffold NAME' to create entire mvc structures with migration files</li>
<li>Configure models to have proper associations and validations</li>
<li>Create tables with 'rake db:create_migration NAME=table_name'</li>
</ol><br>
With the foundation of the app complete, I was able to move on and start working on my routes. This is where consideration for the user experience comes into play for me. Personally, I like visuals and readable figures so my dates, balances and navigation had to be the most-user friendly I could create. I found a  <a href=https://www.educative.io/edpresso/how-to-create-columns-in-html>site</a> that would then let me create columns in HTML to be able to include a menu for navigation.<br>
The next aspect I wanted to make sure was legible was the date, so I changed the datatype of my balance columns in my bills table within my migration folder to 'decimals' and formatted the output in my views folders to show two decimal places:
```
<li>Amount Due: <mark>$<%= "%.2f" % @bill.amount_due %></mark>
```

<br>
My date output also needed some adjustment, so I made sure that the full month name, day and year were written out 

```<li>Due Date: <%= @bill.due_date.strftime("%A, %b. %-d, %Y") %>``` <br><br>

<br>
The menu includes the options to show all of the user's bills, create a new bill, show the included calendar, and the option to log out that clears the current session and effectively assures that the user must log in again with the same credentials to view the same information as before.<br>
If there is anything I could add to this project it would be the ability to send the user push notifications to remind them of upcoming pending payments, enabling a more efficient app. I hope that I can learn how to add this feature soon! 

