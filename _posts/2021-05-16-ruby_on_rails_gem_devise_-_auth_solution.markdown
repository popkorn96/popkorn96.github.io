---
layout: post
title:      "Ruby on Rails Gem: Devise - Auth Solution"
date:       2021-05-17 01:36:36 +0000
permalink:  ruby_on_rails_gem_devise_-_auth_solution
---


Devise is one of the many authentication gems available to software engineers. I am using this particular gem for my current project as it does require user authorization and authentication. It has creative flexibility with its many specs including some very useful controller filters and helper methods. <br/><br/>
For gems like these it is always suggested that you try to build an authentication system on your own. This way, you can familiarize yourself with the different aspects that need to be considered when building a authenticator. <br/><br/>
These are a few controller helpers that you could find useful when creating your app with Devise:<br/><br/>
* `user_signed_in?`
* `current_user`
* `user_session`

It's important to note that the 'user' is the name of the model you are implementing your authentication on. For example, if you have just an admin and you choose to create an 'admin' model, the helper methods would need to be created using this naming model. <br/><br/>
##### *OmniAuth*
This gem is also compatible to use with OmniAuth which lets users login through a third party site, most commonly used apps are Facebook, Google, and Twitter but there are many other providers out there available to use with OmniAuth.  To customize your app to include OmniAuth with the Devise gem, customize your OmniAuth configuration in `config/initializers/devise.rb`  .<br/><br/>
`
config.omniauth :github, 'APP_ID', 'APP_SECRET', scope: 'user,public_repo'
` <br/><br/>

If you are like me and are creating an app which only requires an admin login, you can build your authentication system using Devise with the following specifications: *The migrations are assuming you are using SQLite*<br/>

```
// Create a migration with the required fields
create_table :admins do |t|
  t.string :email
  t.string :encrypted_password
  t.timestamps null: false
end

// Inside your Admin model
devise :database_authenticatable, :timeoutable

// Inside your routes
devise_for :admins

// Inside your protected controller
before_action :authenticate_admin!

// Inside your controllers and views
admin_signed_in?
current_admin
admin_session
```

As this was a very brief introduction to the many different ways to implement the Devise gem, you can find more documentation [here](https://github.com/heartcombo/devise). Hope this helped any aspiring engineers out there and hope to write again soon!
