---
layout: post
title:      "Rails Project - Build Something"
date:       2018-07-25 23:42:14 +0000
permalink:  rails_project_-_build_something
---


One of the things that initially helped me wrap my head around object-oriented programming was thinking about objects as real, physical objects. To call a method is just to ask a thing or group of things about themselves. With this in mind, I thought I’d make it a bit easier on myself with my rails project by creating a content management system meant to track real-world objects as opposed to something more abstract. 

My app allows users to create and share their woodworking projects by creating a project with instructions and adding materials required for that project. And, while it was helpful to hold on to my initial scaffolding concept, I soon learn it was limiting and presented some challenges. Moving from a CLI project to Sinatra, and finally to rails, much of what is actually taking place within the code is abstracted away. Creating complex associations requires a bit more flexibility of thought, so it’s no surprise that the most significant challenge I encountered was in creating a nested form. Sure, form helpers allow you to complete complex tasks quickly. They might even seem like magic. But it doesn’t always seem like that when you’re learning how to use them.

Building a more complex form with four models requires that you to strip away the abstraction and look at what the helpers are actually doing. It’s not as easy to user rely on the “real world” analogy when you have to look at the form itself as an object building out not only attributes of your object, but also attributes of objects to be associated in multiple different ways. I found the only way to do this is to spend a lot of time looking at the data I was passing through my form. Materials_Attributes? Where did that come from? And then looking at the html to see that – no, it’s not magic. 

Input type= “text” name=”projects[materials_attributes[0][name]” id= “project_materials_attributes_0_name”>

Ultimately, it’s an extremely useful way to organize your data, lending itself to easily accessing its pieces. 
It can be difficult to recognize how much faster projects can move with these abstractions when what you’re building is more complex than what you’re used to. Still, it might be that learning during these huge leaps in functionality means slowing down even more. This project showed me that making the best use of rails magic means understanding how it works.

