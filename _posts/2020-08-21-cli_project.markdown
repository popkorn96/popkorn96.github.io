---
layout: post
title:      "CLI Project"
date:       2020-08-21 12:18:06 -0400
permalink:  cli_project
---


I got through it! I got it to work! - These were my first thoughts whenever I first got my CLI project to work and it felt incredible, knowing that I was able to implement the things I've been learning for the past few weeks into a personalized project with functionality was honestly one of the proudest moments of my life, there was nothing to bring my mood down since then. For those of you just starting the project out, please don't ovethink your solutions, there are many resources online that help you understand methods like scraping or looping if you haven't fully grasped those yet, and many others.
Starting this project with a clear idea of what I wanted the app to do was key to getting the ball rolling and getting everything in its place. Scraping was challenging at first but once you grasp the concept and retrieval proceedures you can definitely get it done and this experience will help in a long run as well. I HIGHLY recommend testing out your code as you go, I personally used the REPL.it site to verify that my scraping was on the right track and I used PRY to make sure my code was okay. The project was a very rewarding experience and while it was nerve wrecking at first, I was proud of my end result!
All in all, my project focused on the user's experience. I knew what my information my user needed to see and planned my paths accordingly. 
My app, Anime 2020, first welcomes the user then prompts the user to input '2020' to display all anime premiering in 2020. Once the user enters '2020', this app shows the list of anime. Once the user chooses an anime from the list, they can input the reference # which then prompts the app to display a description and release date for that anime. The user can then choose to see the list again or quit the application. Visually, the user will see the following promtps:
1. Welcome message
2. Please enter '2020' to see all 2020 anime => (Displays anime list)
3. Please choose an anime by number to see more info about that anime=> (Displays anime name, description, release date)
4. Enter 'back' to see the list again or enter 'exit' to quit the app
5. Goodbye message

In the future, I would like to add another level in which the user can see the list of anime organized by genre so that the full alphabetized list doesn't look so overwhelming. If I do get around to doing so, I would structure my CLI class's list_anime method differently to display the list of anime by genre if the input were 'genre' in step 2 of the user prompts, as shown below:
```
    def list_anime
        puts ""
        puts "✧･ﾟ: *✧･ﾟ:* 　Welcome to Anime 2020!　 *:･ﾟ✧*:･ﾟ✧ "
        puts ""
        puts ""
        puts "~ This app lists anime that premieres in 2020!"
        puts ""
        puts "~ Enter '2020' to see the complete list of anime ☆"
        #puts "Type 'genres' to see the genres of the upcoming releases :)"
        puts ""
        input = gets.strip 

        case input 
        when "2020"
            puts ""
            puts "~ Anime by alphabet coming up! (〃＾▽＾〃) "
            puts ""
            sleep(2)
            self.list_all_titles_alph
        when "genre" #<= changes would be here 
            puts ""
            puts "Genres coming up!"
            puts ""
            sleep(1.5)
            self.list_genres
        end
    end
```

You may notice that I included the sleep method to delay the displayed lists. The purpose of this was to allow the user to read each prompt and message without having to rush. As I was testing out the program, I realized that if the list were displayed immediately, the welcome message would be instantly lost and the user would have to scroll up to see the welcome message. Always test your program for the user's experience (after functionality of course) to ensure that your user has the best possible time using your app.

