---
layout: post
title:      "React-Redux Final Project"
date:       2019-02-18 18:20:33 +0000
permalink:  react-redux_final_project
---


My React-Redux final project was a challenging culmination to the work I’ve done with Flatiron. As always, I found that creating a project from scratch was the best way to cement my understanding of the topic. While the curriculum and labs helped my understanding by zeroing in on specific topics, it can often be difficult to see how it all connects. The final project was a great opportunity to use everything I have learned and, I think most importantly, forced me to spend countless hours poring over documentation. With the curriculum at an end, it seems clear that this is one of the most valuable skills I’ve learned.

For my final project, I made a simple flashcard app because it is something I intend to build on and make part of a larger learning platform. The app allows the user to login and create decks and cards to review for memorization. As with my other projects, my first challenge was simply with handling the configuration. There was significantly more setup involved with this project, as it essentially involved making two apps – a client and an API. While setting up the Rails API was relatively simple, I found my first difficulty was in understanding how the client and API application flow stayed in sync. Routes, for example, were confusing to me because I was used to Rails handling URLs. I also found it difficult at first to persist a user through a session – a problem for which there seems to be many solutions. Finally, it was more challenging conceptually to manage data flow back and forth from the client than simply within a Rails application.

With little experience using a language, library, or framework, it can be difficult to plan far ahead. With React and Redux, there was a lot of trial and error with async requests and managing data flow through my application. I had a similar experience with my Rails and Rails with JS projects – making mistakes that became clearer only once they started breaking my app. 

Ultimately, my React code came down to four processes – Create, Fetch, Map, and Display. I used controlled forms for the creation of Users, Decks, and Cards and fetch requests to the index action in my Rails API to return all of those cards. Then, I used container components to map over my data and send it to their corresponding presentational component. 

My goals for expanding this app include adding more functionality to allow for spaced repetition, so users are seeing flashcards that they find difficult more frequently. This, along with more detailed styling can make the app more natural to use. I’d also like to add stronger user authentication, as my current version using a simple password match solution. 

