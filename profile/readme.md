![image](https://user-images.githubusercontent.com/73878099/172373718-1e27b565-88ea-44ab-bbdc-255b3256cc2f.png)

># Stokers Portfolio🧾
By: Rens Vlooswijk

For: Cv De Stokers and Fontys Semester 3

# Table of Contents:
### [1. Introduction](#3-research)
### [2. Learning outcomes](#2-learning-outcomes-1)
- [2.1 FullStack](#1-fullstack)
- [2.2 Software Quality](#2-software-quality)
- [2.3 Agile](#3-agile)
- [2.4 CI/CD](#4-cicd)
- [2.5 Cultural differences](#5-cultural-differences)
- [2.6  Requirements](#6-requirements)
- [2.7 Business process](#7-business-process)
- [2.8 Professional](#8-professional)

### [3. Research](#3-research-1)
- [3.1 Ethics](#ethics)
- [3.2 Agile methods](#agile-methods)
- [3.3 How to obsidian](#how-to-obsidian)
- [3.4 Security](#security)
- [3.5 Cultural Differences](#cultural-differences)

### [4. Reflection](#4-reflection-1)
- [4.1 What went well?](#what-went-well)
- [4.2 What could have gone better?](#what-could-have-gone-better) 

# 1. Introduction
This project is a website for the carnaval's association "De Stokers".
It is meant to attract more members to the association and to plan and see all upcoming activities that they are going to partake in. Plus you can see pictures and videos of previous activities and specials like the "Mooi man" cover and a carnaval press conference.
I chose for this project because we just started the association and we still needed a website so I could combine my semester with this.
The project uses a [react](https://reactjs.org/) frontend and a asp.net API that manages the activities.
Furthermore it uses the instagram and YouTube API to show the Stokers instagram feed and its YouTube specials.

# 2. Learning outcomes
## 1-FullStack
>### - _"You design and build **user-friendly**, **full-stack** web applications."_
>
>#### Clarification:
>_User friendly_: 
>You apply basic User experience testing and development techniques.
>
>_Full-stack_: 
>You design and build a full stack application using commonly accepted front end (Javascript-based framework) and back end techniques (e.g. Object Relational Mapping) >choosing and implementing relevant communication protocols and addressing asynchronous communication issues.

### Design

When I first started the project I created a class diagram, but as my project expanded I realised this was not enough of a design. So throughout the semester I created and improved a c4 diagram (with a class diagram). The main reason for this diagram is that if I would not be able to finish the project it would be easier for someone else to do so.

![C4 DiagramWithBg](https://user-images.githubusercontent.com/73878099/174475957-74e007ea-20d8-4066-8cc0-d7370e22d7a7.png)

### Front-End

#### The most answered feature to the question "What would you like to have on the website" the most common answer was to see the upcoming activities. So this was my main priority. So now the main feature of the website is the activities tab, on here you can see all the Stokers activities and "join" so the event planners know how many people are going to come. If you are a Stokers member and not just a user of the website you can also add an activity. For example if you are going to throw a carnaval related party of some sorts you can create this as an activity on the website.
#### Another item on the frontend is the YouTube video's. the Stokers created a song cover and a carnavals press conference, which you can see on the website. 

####  All of this together looks like this:
![FrontEndTour](https://github.com/StokersWebsite/.github/blob/8db5542a91276711fdff3c9b59a83044502f7d3f/Images/FrontEndTour.gif)

#### For my "second frontend" I created an auth0 login, The idea was that Stokers members have an account and can login while other users can not make an account.

![image](https://user-images.githubusercontent.com/73878099/173632445-2d1441bf-ae08-4416-a414-1bb82c13588c.png)

#### I made this using [React](https://reactjs.org/) JS because I had never used Javascript and I would love to learn it since it is growing in popularity and it seemed to be handy in the future.

#### To check out all the code go to [Stokers Frontend](https://github.com/StokersWebsite/StokersReactWebsite)

### Back-End
#### For the websites backend I used ASP.Net / C#. I picked this because I already had experience with this and since I already picked a (for me) new frontend framework and language I felt like this was the best option. Because this way I would still learn a lot of new things but I would also be able to have some functionality. For the group project we chose for a micro-service structure but this would be over engineering, which would be a waste of time. That's why I just have 1 API which can get all the activities and add new activities.
![Swagger Gif](https://github.com/StokersWebsite/.github/blob/1899216aaaadb96c6db2d5a38fde6bf4e5d6e958/Images/swagger.gif)

#### To see the API's code go to [Stokers API](https://github.com/StokersWebsite/StokersDataTransferService)

[Back to table of contents](#table-of-contents)

## 2-Software Quality
>### - _You use software **tooling and methodology** that continuously monitors and improve the software quality during software development._
>
>#### Clarification:
>_Tooling and methodology_: 
>Carry out, monitor and report on unit integration, regression and system tests, with attention for security and performance aspects, as well as applying static code >analysis and code reviews.

#### To complete this I used [Sonarcloud](https://sonarcloud.io/), This checked my code each time I pushed something to git. I chose for this type of static code analysis since I usually create "Messy" code. I don't always remove my commented code that I am not going to use. And import things that I then don't use. This way I could easily find those things to clean up my code. And so I did. I had personally never heard of Sonarcloud before the semester but I think it is really useful and I am definitely going to use this again, since it improved my code quality for sure.
![Sonarcloud](https://github.com/StokersWebsite/.github/blob/122b0a672e74e3130e2b491cc79e022a74f50596/Images/Sonarcloud.gif)
#### Another thing Sonarcloud picked up are some Security hotspots. It says my API is vulnerable since it is publicly accessible for everybody. But this is exactly the point since otherwise my own frontend wouldn't be able to use it either. So these 2 security hotspots are neglectable.
#### To test if my API was working as intended I mainly used postman. This too was a good choice and will be used again by me for sure. It helped tremendously when my activities would not load and I thought something was wrong with my API. But after using postman I found out this wasnt the case. Then I used Sonarcloud to find the bug which was in my frontend. Before this semester it would have taken me way longer to find this bug, but thanks to the (for me) new tools it was a quick fix.
![Postman Demo](https://github.com/StokersWebsite/.github/blob/594875f9ec52fb7b295ea3c71fe8390a96cf5e01/Images/PostmanDemo.gif)
#### In postman I also made intergration tests for my API, I chose for intergration tests in postman rather than testing the logic layer of my API since it doesn't have that much logic functions, so it wouldn't be useful.
These tests could also work as unit [regression tests](https://www.guru99.com/regression-testing.html) by running it daily (or weekly) but that doesn't work if it runs on docker (locally).
![postman tests](https://user-images.githubusercontent.com/73878099/174308123-ae2aa45b-fc30-487e-b132-87d3308b081d.png)
)
### [Eeventify](https://github.com/Eeventify)
#### For the group project we also made integration tests, We felt like this was the most useful test since this was the best way to see if everybody's code could work together.
#### And we also monitored the status of the application, We did this because the application runs on a group members home server and this way we could check if it was still working.
![[image]](https://github.com/StokersWebsite/.github/blob/e0bd499b9bc15a84ee4a9c0c9c5e085e1f7ff7a8/Images/eeventify_postman_monitor.png)
#### As of this semester I learned a lot of new tools to improve my software quality. I feel like I used these to the best of my ability.

[Back to table of contents](#table-of-contents)

## 3-Agile
>### - _You **choose** and implement the most suitable agile software development method for your software project._
>
>#### Clarification:
>_Choose_: 
>You are aware of the most popular agile methods and their underlying agile principles. Your choice of a method is motivated and based on well-defined selection criteria and context analyses.

#### For the group project we used Scrum as our agile method. We did this using Taiga. This is a program that allows you to make a board per sprint that has all tasks which you can assign to people. We chose scrum since the Finnish students had used this method before and would like to do it again. We also discussed Kanban but the main reason we didn't chose this is that it isn't based around sprints. For us sprints were very useful since it allowed us to check our progress every few weeks since we had no idea how this project would go. The cooperation with the Finnish students made it really hard to estimate all tasks we would be able to finish.
#### We used taiga as our scrum software and had a taiga project for the front-and-back end so we could see each others progress. None of the dutch students had ever heard of taiga but our teacher and the finish students were very positive about it so we decided we would try it out.

![TaigaBoard](https://github.com/StokersWebsite/.github/blob/dd00cefd4046c3a1ebfb5f568a243db58f544672/Images/TaigaBoard.gif)

#### I also wrote a research document about agile and scrum: [[📄Agile]](https://github.com/StokersWebsite/.github/blob/31c1068a435684bf41054adccb10a86c87268d3d/Research/Agile.md)

[Back to table of contents](#table-of-contents)

## 4-CiCd
>### - _You **design and implement** a (semi)automated software release process that matches the needs of the project context._
>
>#### Clarification:
>_Design and implement_: 
You design a release process and implement a continuous integration and deployment solution (using e.g. Gitlab CI and Docker).

#### First of all, this was completely new to me and I learned a lot, Again with the new tools to help me make better projects. 
#### To set up my Ci/Cd pipeline I used github actions and docker. This was recommended to me by fellow students in my group project, which I am incredibly grateful, since it was a very good suggestion and I am very likely to use it again for future projects. 
#### Now, whenever I push any new code to my main branch it would (try to) build the project. If this is successful it will run all the tests in the test project layer. And if all of these are successful as well it will deliver everything to docker hub from where it will deploy it on docker desktop.
#### To see everything it does check out my [CI/CD yml File](https://github.com/StokersWebsite/StokersDataTransferService/blob/91455fa628611ab7de7c4412e441462df6672c92/.github/workflows/MainCI.yml).
#### I then end up with a docker container that has the front-and-back end as well as the database (so everything). It all runs and works together to make a fully functioning website which I am relatively proud of. At the start of the semester I didn't think I could get this to work as well as it does but here we are.
![CD github action](https://user-images.githubusercontent.com/73878099/174228374-16c8fa91-78bf-4311-98b8-4fca2afc1084.png)

![[image]](https://github.com/StokersWebsite/.github/blob/f237d7180f1d9e2dd15e4b0b298508afa0b6a7ee/Images/DockerRunning.png)

[Back to table of contents](#table-of-contents)

## 5-Cultural differences
>### - _You **recognize** and **take into account** cultural differences between project stakeholders and ethical aspects in software development._
>
>#### Clarification
>_Recognize_ : 
>Recognition is based on theoretically substantiated awareness of cultural differences and ethical aspects in software engineering.
>
>_Take into account_ : 
Adapt your communication, working, and behavior styles to reflect project stakeholders from different cultures; Address one of the standard Programming Ethical Guidelines (e.g., ACM Code of Ethics and Professional Conduct) in your work.

### Finland
#### For me the cultural differences were very visible since I worked on the Oulu project with Finnish students. I feel like that we as dutch students inherited a lot of the Finnish ways of doing things. Like taiga, We had all never heard of it, but since the Finnish students had, and liked it we decided to use it for this project as well.

### Ethics
#### For ethics we had to think of ways that our application might affect its users.
#### Our group application is a social media application, As such our users would be able to chat with each other. This in and of itself could be problematic since it could be used to insult other people. Our application is also based on group activities, this means users could exclude other users from a certain activities, this would [inflict harm](https://www.acm.org/code-of-ethics#:~:text=locally%20and%20globally.-,1.2%20Avoid%20harm.,-In%20this%20document) to other users using our software.
To see more about ethics check out [[📄Ethics research]](https://github.com/StokersWebsite/.github/blob/31c1068a435684bf41054adccb10a86c87268d3d/Research/Ethics.md)

[Back to table of contents](#table-of-contents)

## 6-Requirements
>### - _You analyze (non-functional) requirements, elaborate (architectural) designs and validate them using **multiple types of test techniques**._
>
>#### Clarification:
>_Multiple types of test techniques_ : 
You apply user acceptance testing and stakeholder feedback to validate the quality of the requirements. You evaluate the quality of the design (e.g., by testing or prototyping) taking into account the formulated quality properties like security and performance.

### Teachers
#### I had multiple stakeholders including my teachers, cv de Stokers members and myself.
#### For the "user acceptance" of the teachers I of course had feedback moments and casual conversations (with Leon) about my project and progress. I did this because then I got to know more about what still had to be done. And I got some good tips on how to move forward.
#### But it already started with the project idea, my teacher (Leon) was a big fan of picking a project which you would enjoy, instead of a basic project just to complete the learning outcomes. This is exactly what I did by making a website for the Stokers. This in and of itself was stakeholder feedback that indirectly made the requirements.
![[image]](https://github.com/StokersWebsite/.github/blob/e0bd499b9bc15a84ee4a9c0c9c5e085e1f7ff7a8/Images/Feedpulse.png)
### Stokers members
#### I also got feedback as user acceptance testing from Stokers members, first of all about the requirements of course. I did this at the start because I wanted to know what all the members wanted in the site. 
#### From this I learned that most members would like a activities tab on which they can see what events are coming up, which I then added to the requirements.

![[image]](https://github.com/StokersWebsite/.github/blob/e0bd499b9bc15a84ee4a9c0c9c5e085e1f7ff7a8/Images/Activity%20requirements.png)
#### I also made user stories to know exactly what the website should be able to do?
![user story 1](https://user-images.githubusercontent.com/73878099/174552479-ca77bc71-bb7e-4857-8839-c950cda420fb.png)
![User Story 2](https://user-images.githubusercontent.com/73878099/174552590-da8ca1ed-1f82-4baa-a9c9-8e39b6430b46.png)
![User Story 3](https://user-images.githubusercontent.com/73878099/174552783-8e03b2b4-f225-41eb-a1c7-5d0686df7137.png)

### [Eeventify](https://github.com/Eeventify)
#### for the group project we planned everything out way better than for my personal project, we made a lot more diagrams and discussed the requirements (while in Finland) extensively.
![image](https://github.com/StokersWebsite/.github/blob/bfdb67662045b1986345ef1bd5f140006d0e8c87/Images/unknown.png)

[Back to table of contents](#table-of-contents)

## 7-Business process
>### - _You analyze and describe **simple** business processes that are **related** to your project._
>
>#### Clarification:
>_Simple_ : 
>Involving stakeholders, predominantly sequential processes with one or two alternative paths.
>
>_Related_ : 
>Business processes during which the software that you are developing will be used (business processes that the software must support by fully or partially automating >them).
>or
>Business processes needed for the success of your software development project (e.g., product release, market release, financial assurance).

(to be added)

[Back to table of contents](#table-of-contents)

## 8-Professional
>### - _You act in a **professional manner** during software development and learning._
>#### Clarification:
>_Professional manner_ : 
>You actively ask and apply feedback from stakeholders and advise them on the most optimal technical and design (architectural) solutions. You choose and substantiate >solutions for a given problem.

### [Eeventify](https://github.com/Eeventify)
#### The most of my professional skills were developed and shown in the group project (called Eeventify). First and foremost I went to Finland to establish the communications and setup the project. We decided to use discord as our main communication platform. We also exchanged numbers to make a group chat.
#### Together with all the dutch students we also set up a "definition of done". And we verbally agreed on a code of conduct. 
#### Since we didn's work for a company (and we were our own stakeholders), we only really had to communicate with the Finnish students and our other teacher (Bert).
#### We were all very up to date on what the rest of the group was doing although we maybe should have paid more attention to what the Finnish students were doing.
#### We did have sprint meetings every 3 weeks from which we received feedback from both the Finnish students and the teachers.

[Back to table of contents](#table-of-contents)

# 3. Research🔎
As of research I did for this semester:
## Ethics in software 
As in most things ethics, also apply when creating software. You may think ethics aren't a big  deal in software development, but you would be mistaken.
There are a lot of choices when developing software based on ethical and moral choices. To see my full ethics research:

[[📄Ethics research]](https://github.com/StokersWebsite/.github/blob/main/Research/Ethics.md)

## Agile Methods
There are more than one correct agile methods that you can use for a group project. We chose for Scrum, to learn more about scrum and other agile methods:

[[📄Agile]](https://github.com/StokersWebsite/.github/blob/main/Research/Agile.md)

## How to obsidian
For my personal research this semester I chose "How to obsidian". My teacher recommended that I start using obsidian, and so I did. 
I liked it so much that I wanted to do my research about it too. 
To check that out:

[[📄 How to Obsidian]](https://github.com/StokersWebsite/.github/blob/main/Research/Obsidian.md)

## Security
This semester I also learned a lot about security, And especially on what to do about security for specific types of project. This is why my security research is (primarily) about what my project needed for security.
To see this:

[[📄 My Security]](https://github.com/StokersWebsite/Documentation/blob/master/Semester%203/Individueel/Stokers/Research/Security.md)

## Cultural Differences


[Back to table of contents](#table-of-contents)

# 4. Reflection

## What went Well?👍
### The project idea
#### usually it is quite hard for me to think of a good and fun project that is the right difficulty. This time however I feel like I picked a great project, since the semester perfectly co-aligned with the start of the Stokers organization. This was a fun project to work on and had the right difficulty level so I could show everything I needed to know this semester, while still being useful as an actual website for the Stokers.

### The learning process
#### I have learned a LOT this semester. I decided to use JavaScript even though I had never done so before. I also learned about Auth0 and docker and a whole lot more external tools and software programs to help me make better projects, And I can go on and on. I even learned some Finnish this semester!
#### I feel like I got the most out of this semester in terms of what I learned, and this will be very useful in the future.

### [Eeventify](https://github.com/Eeventify)
#### The group project also went really well in general, We had great communication both with each other as well as with the Finnish students. In the end everything worked and we had a great time when they came to the Netherlands.

[Back to table of contents](#table-of-contents)

## What could have gone better?👎
### Setup
#### I feel like my setup at the start of the semester was not nearly good enough.
#### I have always had problems with this, I never setup my project correctly. This means I now have multiple folders with similar names and it gets harder and harder to keep track of which is the newest/the correct one. I also started by creating normal repositories, but when it started to get cluttered I made a github organization. This was the better decision and helped me a lot with keeping everything organized. 

### Naming
#### The next consistent problem this and other semesters was my naming of everything. I try to explain the thing it does in the name but this starts to overlap very quickly. After that I get really long names that look alike but have a different word in them, This gets very confusing and needs changing.

### Planning
#### For our group project we started by creating a planning and we divided all the tasks in sprints and it all worked out great. For my individual project on the other hand, I should have made a better planning. I started the project with a kanban board but I never really kept it up to date. I also could have worked on and updated my portfolio throughout the semester.  

>#### Conclusion
>##### This semester was very educational even though there were lots of things that could have gone better. So next semester I will start the project with a better setup and keep everything (more) up to date.

[Back to table of contents](#table-of-contents)

