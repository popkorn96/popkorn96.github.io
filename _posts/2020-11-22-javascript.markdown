---
layout: post
title:      "JavaScript "
date:       2020-11-23 00:33:11 +0000
permalink:  javascript
---


This was one of the funnest projects I have EVER had. I wanted to start on this as soon as possible and had to quickly choose an idea that would best suit the requirements and I decided on doing something festive to celebrate what's comning around the corner. I have so much to be grateful for this year and a big part of it has been engaging in this path and sticking to it.<br>
This section has been very fun and very rewarding. At first it seemed odd how the lessons were structured and it even seemed as though some had been switched around a bit but that was okay because gradually, all of the bits started to make sense, in an applicable way. <br>
The easiest part was setting up the Rails API as our server, seeding and generating our resources. Getting all of our information to JSON format was also pretty straight forward with the serializers. Where I began to get stumped was during the times I would have to deal with the fetch requests. Using the GET was simple enough and I had my seeded data on display with JS in just time. Using POST and PATCH, however, was the tricky part for me. <br>
The way I have my forms set up for generating new objects (Characters and Gifts) or editing them, it required me to include my knowledge of how these requests are meant to be processed from back in September when we were first learning about Ruby forms. <br>
Recalling that information wasn't the problem, but translating it into JS was. For reference, here is a snippet of my Server class in my JS frontend. 
```
static postFetchCharacter(name, age, favorite_color){
        return fetch(`http://localhost:3000/characters/`, {
            method: "POST",
            headers: {
                'Content-Type': 'application/json',
                'Accept': 'application/json'
            },
            body: JSON.stringify({
                name: name, 
                age: age,
                favorite_color: favorite_color
            })
        })
        .then(response => response.json())
        .then(json => {
            let newChar = new CharactersAndGifts()
            newChar.renderCharacters(json)
            console.log(`characters rendered..`)
        })
				
    
``` 
Oddly enough I really do think I enjoy fetching now. This function returns the fetch request I made with the option of POST with headers and my JSON stringified body. The request is then completed and my other functions are rendered onto my main screen. Initially, this function did not want to accept the parameters that I provided but that was until I realized that I had been feeding it ```undefined``` lol. <br>
This was all in all a really fun project to complete and like others before it, I want to improve upon this one whenever I get a real chance. 
