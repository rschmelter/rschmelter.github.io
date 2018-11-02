---
layout: post
title:      "Rails with JavaScript Project"
date:       2018-11-02 16:55:35 +0000
permalink:  rails_with_javascript_project
---


Integrating JavaScript, jQuery and AJAX into my Rails project, it finally seems as if I’m beginning to have the necessary tools to build a legitimate modern web application. What’s interesting is understanding exactly how necessary it is to keep track of every decision that is made. Seemingly minor decisions, such as giving a div an id attribute instead of a class attribute can have significant implications, causing you to have to check the code line by line to see exactly what went wrong.

Of course, getting it all to work is very satisfying. It’s incredibly powerful to be able to add dynamic features that offer a seamless experience for the user. That said, I wanted to take a look at just a small piece of my code that illustrates how dynamically manipulating the DOM requires extra attention to detail and a commitment to flexibility from the outset.
My project is a woodworking management app that allows users to add the projects they created along with instructions and all the materials needed to create them. My goal was to be able to dynamically load a users’ projects from their Show page, rather than redirect. The first step is to provide a truncated list of all the users’ projects, accessing the has_many relationship, and providing a bit of introductory information to avoid adding an overwhelming amount of information to the page. Then, once the list of projects is loaded, allow the user to click a link to dynamically display the full project – again without being redirected. This presented my first challenge. I not only needed to render content dynamically – I needed that dynamic content to create links to more dynamic content. 

The first part was easy enough – hijack the link to the projects index endpoint, render the content as JSON and then display it on the page. The first thing I noticed was that, if I wanted dynamically created links that pointed towards a show endpoint, I needed a way to identify those links. My solution was to dynamically generate ID attributes for each link by interpolating the object ID. First problem solved.

Additionally, the dynamically created content did not exist on the initial page load. Embedding the AJAX call in an anonymous function is equivalent to using .ready(). But since these functions can only bind to pages upon loading, a different solution was needed for the dynamic content. Here’s how I addressed it:
```
$(function(){
    
    $("body").on("click", ".full_project", function(e){
        e.preventDefault();
```


I’m looking forward to rebuilding this app from scratch once I’ve further developed the tools to create a more flexible approach. 

