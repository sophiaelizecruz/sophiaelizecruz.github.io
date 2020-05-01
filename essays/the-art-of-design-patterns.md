---
layout: essay
type: essay
title: "The Art of Design (Patterns)"
date: 2020-04-30
labels:
  - Design Patterns
  - Software Engineering
  - Object Orientation
---

>> Work smarter, not harder.

## Consider The Beauty Within
When thinking about design patterns, a lot of people immediately think about the aesthetics in terms of art and refer to 
principles of design that leans more art and graphic design. However, in software engineering and in a lot of disciplines 
where you would least expect it, design patterns are an integral part of the success and functionality of the projects that 
engineers produce and maintain. When implementing these applications, software engineers refer to certain aspects of design in 
order to produce a system that is efficient, organized, and makes the development process run smoother by referring to certain 
design patterns. After all, while getting the semantics and the solution is impressive, there are many more efficient 
solutions to consider that make your solution much more elegant and understandable and will make you stand out from other 
programmers. It's kind of like doing a puzzle, or playing Jenga: where should I put this piece, and how will it affect the 
overall outcome?

## The "Problem": "Design Patterns. Yikes."

Design patterns are solutions that can be reused to commonly occurring problems in software design, and provide a sense of 
organization and elegance during the development process. When describing a design pattern, a software engineer must recognize 
what their task is, consider the patterns relevant to the task at hand that can be used to solve the problem, and from there, 
weigh out the positive and negative consequences for each possible solution. Software engineers should able to understand and 
view the relationships and interactions between objects and classes, and some of these patterns include the creation of 
objects, how we represent collections of objects, as well as how these objects behave by themselves and with other objects 
with each pattern. Some common examples of design patterns are factory, singleton, observer, and the model-view-controller 
the problem, in which the model-view problem has different approaches such as the model-view-adapter (MVA).

In introductory computer science classes, students will more often than not encounter the factory and singleton pattern. The 
factory pattern provides the leisure of being able to return objects associated with different classes, and in a sense, that 
provides a level of efficiency. However, we must consider that despite its welcoming nature, it can be more complicated than 
an object-oriented class constructor. Another common pattern that new students encounter is the singleton pattern, in 
which it provides a global variable to an object-oriented language that would otherwise not support global 
variables or a complex global state. Alongside that, singletons only allow one instance of a class to to exist. While it does 
allow developers to implement lazy initialization, the use of singletons and global variables in practice is unwise and is 
not thread-safe, so new programmers should be careful to not develop a bad habit of relying on this pattern.

Some of the other patterns that a software engineer may encounter are the observer pattern that is common in event-driven 
systems such that you must provide one or more "event-handlers," and it easy by remembering the fact that it handles states 
and has a messenger-like structure that notifies the other objects whenever there is a state change. While it eliminates the 
need for tight coupling and provides a sense of organization and flexibility in informing other objects and that it allows for 
dependencies to be changed at runtime, it may cause issues in multi-threaded systems, and a poor understanding of it may lead 
to complications in debugging as well as a subpar performance. 

One of the more intimidating patterns would definitely be the model-view-controller pattern, in which we split up the internal 
representation of information from the way that the user views and accepts it. Breaking it down, the model encapsulates the 
database aspects, the view is the management of the visual components and aesthetics via HTML/CSS for the application, and the 
controller handles the behavioral aspects of the problem. The beauty of this pattern is that the tasks can easily be 
distributed among team members such that there is a group that specializes in a certain aspect, whether it is in UI design or 
database design, to other aspects of the task at hand. However, this requires that each person must know the ins and outs of 
their specialty, which may seem daunting, but at the same time, exposes how much passionate and willing a person is to further 
their knowledge on the subject that they focus on, which is what separates a good programmer from an exceptional programmer. 

Reading about these design patterns are only one side of the coin; a person can memorize them all they want, but it's when 
they experience them and practice them, that they really start to develop their problem-solving skills. Without the proper 
skills and strategies for problem-solving, one may engage in antipatterns. Imagine thinking that your solution is foolproof, 
only to find that it has little to nothing to do with the task at hand. It's like going to an interview, except that when you 
show up, you come to find that it was supposed to be in another town and that you were supposed to be there three hours ago. 
How embarrassing.

## The Solution: "Think Like A Computer Scientist."

While design patterns may seem intimidating, it is just a matter of adapting to a certain mentality when approaching the 
problem. Having used singletons and factory patterns in introductory courses, I now see how knowing and practicing these 
patterns constantly will help the development and design process go by much smoother. Design patterns are definitely something 
that should not be looked over and should be something that every software engineer should want to know by heart. With the 
activities that we do in class, especially with this final project and eventually other group projects in both academic and 
professional settings, we follow the model-view-controller pattern in which we designate tasks according to a team mate's 
strengths and weaknesses, and use this knowledge to easily distribute tasks throughout the project (for example. for me, who 
leans more towards UI design, I had been involved with a lot of those aspects in designing and implementing our group's 
application.) By experiencing these design patterns through classes and projects outside of them, you are essentially 
developing a toolbelt of tips and tricks that you can apply to similar situations that you may encounter in the future.
