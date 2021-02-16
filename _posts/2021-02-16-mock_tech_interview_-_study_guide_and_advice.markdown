---
layout: post
title:      "Mock Tech Interview - Study Guide and Advice"
date:       2021-02-16 17:19:53 -0500
permalink:  mock_tech_interview_-_study_guide_and_advice
---


   Most of the time, job-seekers in the software development field are given the recommendation to complete a mock technical interview to prepare for what a real technical interview might look like when applying for developer jobs. These mock interviews are given to test a potential hire on their foundational knowledge of a programming language, arithmetic problem solving ability, and perhaps framework or library familiarity. There are countless resources available online, and luckily I found an instagram account that posted a [study guide](https://docs.google.com/spreadsheets/d/124ehfzCzZc-eXLAhwLJx5dXo7ooc7RV_qlodSEvMT58/edit?usp=sharing) for a basic tech interview (by [@champagnecoder](http://www.instagram.com/champagnecoder/)). <br>
	 
There are also a few resources that help coders practice algorithm problems, some of which are:
* [Code Signal](https://codesignal.com/)
* [Leetcode - FIS DSA 100+](https://leetcode.com/list/5r99deem/)
* [AlgoExpert](https://www.algoexpert.io/questions)
* [HackerRank - Data Structures](https://www.hackerrank.com/domains/data-structures)
* [CodeWars](https://www.codewars.com/)


<br>
   There are some employers that prioritzie the Data Science and Algorithm (DSA) portion of the interivew, but others prefer that their potential hires have a strong foundation in their chosen languages. I had my interview for JavaScript and React and to my surprise, the interviewer had more interest in my familiarity with the framework rather than the language. Luckily it was the mock interview but I was very *very* humbled. I realized I needed a firmer understanding of each of the principles of the languages I worked with, it was not enough to produce a result. <br><br>
So many different companies require different language specialties and it can become difficult to figure out which jobs to apply to that require your specific skill set. While it may be tempting to attept to pick up another language, **don't**. It would be wiser to hone the skills you already have. 
	 
	 
> 	 “I fear not the man who has practiced 10,000 kicks once, but I fear the man who has practiced one kick 10,000 times.”
> 	 - Bruce Lee
> 	 

<br>
My focus moving forward is to hone the skills I already have and understand the principles of each language and framework I have worked with. My intervewer told me that to practice, I could pretend to explain each bit of code to a 5 year old asking 'why' continuously. I started working bacwards from my understanding of React and Redux, going back to my beginnings in Ruby. Finding a job in these times is difficult to say the least, but we can leave the interview feeling confident in our foundational knowledge as opposed to scattered focus. <br>
## React Review
Below are just a few points I think are crucial to review before your next React interview: <br>

1. What is the purpose of lifecycle events? How are they used?<br><br>
   *Each component in React has a lifecycle which you can monitor and manipulate during its 3 phases*<br><br>
	 *Mounting - Putting elements on the DOM* <br>
	 *Updating - Whenever there is a change to a component’s state or props. *<br>
	 *Unmounting - When a component is removed from the DOM.* <br>
2. How is a callback function used? <br><br>
   *[The purpose of this callback function is](https://medium.com/@thejasonfile/callback-functions-in-react-e822ebede766#:~:text=Information%20in%20React%20gets%20passed,parent%20to%20child%20as%20props.&text=The%20purpose%20of%20this%20callback,This%20closes%20the%20data%20loop.) to change a piece of the state that is a part of the parent component*<br>
	 
3. What is the purpose of callback function as an argument of setState()?([source](https://github.com/sudheerj/reactjs-interview-questions))<br><br>
   *The callback function is invoked when setState finished and the component gets rendered. Since setState() is asynchronous the callback function is used for any post action.*<br>
	 
4. What is the purpose of the render method? ([source](https://github.com/sudheerj/reactjs-interview-questions))<br><br>
  *This method is used to render a React element into the DOM in the supplied container and return a reference to the component. If the React element was previously rendered into container, it will perform an update on it and only mutate the DOM as necessary to reflect the latest changes.* <br>
	
5. What is the ‘virtual DOM’  and how is it different from the regular DOM?([source](https://www.interviewbit.com/react-interview-questions/#react-react-dom)<br><br>
   *The virtual DOM is a concept where a virtual representation of the real DOM is kept inside the memory and is synced with the real DOM by a library such as ReactDOM.*<br>
<br>
There are many resources worth reviewing and it may be difficult to navigate with so much information available, but the important thing to remember is that intvewers **know where you've been** and don't expect you to know absolutely everything. We all start somewhere and what matters is the grit to keep going.

