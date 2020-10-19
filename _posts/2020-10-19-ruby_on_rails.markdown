---
layout: post
title:      "Ruby on Rails! "
date:       2020-10-19 04:57:34 +0000
permalink:  ruby_on_rails
---


This time around was much more challenging for me, in particular the associations, but we'll get to that in a second. Firstly I wanted to say that the magic of Rails is real and humbling. The months leading up to this project had us diving into the foundations of it all and made me see only a fraction of the powerhouse that is Rails. There were gems out there too but I decided to start this project off of Rails and the basic gems line bcrypt and omniauth. <br>
As I mentioned before, the associations really threw me for a loop. Most specifically, the has_and_belongs_to_many association. While I did have my models with appropriate associations, the bigger picture didn't fit within it and I had to switch over to the has_many :through association as a result. I'll put a snippet of code below to explain that transition. 
```
class Assignment < ApplicationRecord
    belongs_to :teacher
		has_many_and_belongs_to :children
end
```
<br>
```
class Child < ApplicationRecord
    belongs_to :classroom
		has_and_belongs_to_many :assignments
end
```
<br>
This should have worked for me and let me assign as many assignments to as many children as I wanted, but the naming did not let me. The plurality of 'children' threw me completely off throughout my project and stalled me almost completely. Had it not been for the Rails guide I really would have had to start over 3 days into the project. I was able to get everything in order by doing the following: <i>(If you plan on following suit, I strongly suggest doing this in order</i>
<ol>
<p>Delete the Assignments and Children tables, doing a has_and_belongs_to_many requires you to make a join table whose sole purpose is to carry the foreign keys without having an id itself.</p>
<p>Create a join table with an id and belongs_to datatypes</p>
<p>Review and edit your model's associations to reflect a has_many :through association instead, making sure to include the new join table</p>
</ol><br>
This project almost got the best of me but I pulled through and made something I am extremely proud of!

