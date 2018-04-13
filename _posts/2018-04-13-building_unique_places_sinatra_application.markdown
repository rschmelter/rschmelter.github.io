---
layout: post
title:      "Building Unique Places Sinatra Application"
date:       2018-04-13 21:09:58 +0000
permalink:  building_unique_places_sinatra_application
---

For my Sinatra application, I decided to build an app that allowed users to sign up, add places that they’ve visited around the world, and save the interesting places they’ve found there, such as restaurants and parks. I included three models, the User, the Area, and the Place. Once a User signs up, they can view other Areas that people have visited and select them to find interesting Places that have been found there. They can also add their own Areas that they have visited and add their own interesting Places. 

There are a few interesting things I learned about the nature of planning an application. Although I spent considerable time thinking about the models and how they would interact as well as how a user would interact with the application before I got started, I found there were some discrepancies between how I thought about my code and how the application would actually work. Take an Area for instance. Say a User has visited Rome, Italy – does that Area belong to the User who added it? That’s how my application worked through a has_many, belongs_to relationship. And, so if another User adds Rome, Italy, it would appear twice on the Areas index page. 

I didn’t address all of these issues in the current version of the application, as I was more concerned with gaining a better understanding of the core concepts than with creating a fully realized application. However, it was interesting to think about how much would go into such a project. For example, if I want to eventually separate the relationship between a User and an Area such that an Area, once added, can be claimed by multiple Users, I can go about this in many different ways. I could create a has_many to has_many relationship between Users and Areas, for instance. Or I could create another model entirely – say World – so that when a User adds an Area, it belongs to the World instead of the User itself. Then, I could present checkboxes so that a User can add interesting Places they found to an existing Area without having to worry about duplication. In this scenario, an instance of Place would have to belong to a User and an Area. 

This also had me thinking about the ways that abstraction might allow me to achieve this fully realized version with far less code and in a much dryer way. Specifically, using Sinatra and ActiveRecord provided greater flexibility by giving me access to methods with less code. It’s interesting to see these tools built on top of one another and to consider the flexibility we’ll have with greater levels of abstraction. 

