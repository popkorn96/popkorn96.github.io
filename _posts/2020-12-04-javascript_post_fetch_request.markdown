---
layout: post
title:      "JavaScript POST Fetch Request"
date:       2020-12-04 21:18:39 +0000
permalink:  javascript_post_fetch_request
---


   Working through JavaScript can get complicated fast if you are not familiar with how properly use FETCH requests to either create or update to your API. We have to start out by familiarizing ourselves with the different components that make up a complete FETCH request. For this example, I will build a POST FETCHrequest to show how to update newly created data into your Rails API database.<br><br>
   Using FETCH allows JavaScript to access and manipulate resources asynchronously accross the network. It does those things through **resources** and **requests**.  You can find more detailed information on the different optional properties of FETCH applications [here](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch).
<br><br>
   Firstly, you want to identify the API URL you will be using. My intentions below are to create new Character object with *name, age, and favorite color*  as my parameters, so I will be using my characters route as my API.<br><br>
```
    postFetchCharacter(name, age, favorite_color){
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
```
<br><br>
   The  **```method: "POST```**  is used to send data to a server to create or update a resource. In this case, we are creating a new character. **Headers** contain adittional data that is passed to the API in order to help the server determine what type of request it has to process. The **body** property is used to pass JSON string as an input. It is important to note that headers should be a JSON *object* while the request body should be a JSON *string*.<br><br>
   Secondly, as the information is processing, we must interpret the promise and response. <br><br>
	
	
	postFetchCharacter(name, age, favorite_color){
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
        }).then(response => response.json())     //new code
				.then(data => (console.log(data)              //new code
	 
<br><br>
 These two lines of code will take our the response to our request and give us the updated information in accessable data. <br><br>Here's how:<br><br>

 1. The fetch request immediately returns to us a *promise*. This promise object is a value that represents some data that is not available yet, but that it will be available soon. Other code may run synchronously, meanwhile the promise will display pending until it is fulfilled in the form of a response from the web service that is invoked with the **.then** method.<br>
 2. **.then** is a Promise method that returns a promise fullfilled in the form of a **response**. The repsonse is it's *argument*. The body of data we get from the response is not accessible directly from the response object , so we have to do a few more things. <br>
 3.  We convert the response to JSON using response.json which then returns to us another promise. <br>
 4.  Finally, we implement a final **.then** method and receive the finished JSON data, and in our case we are consol-logging it to test it out. <br><br>

By passing FETCH a REQUEST, we can impliment advanced and customized requests, if you are new to FETCH, I recommend playing around with a PATCH request and see if you can call on a dynamic id, that is if your API allows it.

Thank you for reading! 

