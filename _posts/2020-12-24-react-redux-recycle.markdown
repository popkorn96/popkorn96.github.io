---
layout: post
title:      "React-Redux-Recycle"
date:       2020-12-24 18:09:47 +0000
permalink:  react-redux-recycle
---


   I want to start this post by stating that I have had, **by far**  , the most rewarding experience coding for this latest project. The direction I decided to take this time around was heavily influenced by the fact that this is the last project before graduation. I wanted to go all out and do a fan page for my favorite k-pop group, but decided against it as I do not think future employers would find it as exciting as I do. I went with plan B, a positivity app. These have been stressful times for a lot of us and social media is a boiling pot for advertisements, insensitivity and at times, harsh cruelty. I thought a positive place to go to would be nice, and I came up with positive-point. The idea came from my friend who showed me a site that had nothing but good news, both national and international. He visited the site a lot which explained his unwavering good mood. <br><br>
   I started with a general file and created a Rails API backend and React frontend. I wanted user login capabilities so I didn't use the API tag when creating the backend. Once I had both parts set up, I started installing some dependencies that I required for the project, including redux, boostrap, react-router-dom among a few others. This was when I started thinking of which routes I should create and began working on the Navigation Bar component first. Letting user's see a navigation bar that reflected their login status was a feature I wanted to include and to do this, I had to refer to the react-redux capabilities and my sessions route in my API. I found a way to track a user's status without Redux but I wanted to use the store functionality of Redux to reduce the amount of bugs and promote consistency throughout my routes and events.<br><br>
   Once I had my routes figured out, I started working on individual containers and components. My app model has users, goals, post-its, stories, and comments. At this point, rendering the seed data I created in the API onto each route was the next step. While stories, post-its, and comments are shared data between users, goals are not. The home page is meant to show only the current user's goals. To implement this structure, I used a filter on the goals user_id to match the current user's id, allowing me to then map that data into a goals presentational component (shown below). I followed this flow for additional routes showing the user's post-its and stories. <br><br>
```
{this.props.goals.filter(function(goal, i){
                    return goal.user_id === props.userState.id
                })
                .map((goal, i) =>
                    <GoalListItem key={goal.id} goal={goal} user={props.userState}/>
                )}
```
<br><br>
**Side Note:** I modified the default port that the backend would listen on to receive requests to "3001" , all fetch requests were made to this port while react ran on "3000". <br><br>
From here, I began to work on creating new stories, goals, post-its, and comments. I started with stories and rendered a form on the stories page for debugging. All actions and reducers were placed in a separate redux folder. The submit button on the form would trigger an event listener that would call to the action that makes the POST request (shown below). Based on the response, the reducer would then update the store value to include the newly created story. I plan to include error messages in the near future as well. 
```
export const createStory = (formInput) => {
    return dispatch => {
        fetch(`http://localhost:3001/stories`, {
            method: "POST",
            headers: {
              "Content-Type": "application/json",
              Accept: "application/json",
            },
            credentials: "include",
            body: JSON.stringify(formInput),  
        })
        .then(resp => resp.json())
        .then(story => dispatch({type: "FETCH_TO_CREATE_STORY", payload: story.attributes}))
    }
}
```<br><br>
Overall, I sincerily enjoyed creating this app and would love to continue adding features, options and styling. With more time, I'm certain this could very well be my greatest coding achievement. I implememnted a lot of what I know but I am hungry to learn even more and make my way to becoming a more eager and accomplished developer! 

