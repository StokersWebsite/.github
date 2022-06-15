![image](https://user-images.githubusercontent.com/73878099/172373718-1e27b565-88ea-44ab-bbdc-255b3256cc2f.png)

># Stokers Portfolio
By: Rens Vlooswijk
For: Cv De Stokers and Fontys Semester 3

# Table of Contents:
### [1. Introduction](#3-research)
### [2. Learning outcomes](#2-learning-outcomes-1)
- [2.1 FullStack](#1-fullstack)
- [2.2 Tooling](#2-tooling)
- [2.3 Agile](#3-agile)
- [2.4 CI/CD](#4-cicd)
- [2.5 Cultural Diffrences](#5-cultural-diffrences)
- [2.6  Requirements](#6-requirements)
- [2.7 Business process](#7-business-process)
- [2.8 Professional](#8-professional)

### [3. Research](#3-research-1)
- [3.1 Ethics](#ethics)
- [3.2 Cultural Differences](#cultural-differences)
- [3.3 Agile methods](#agile-methods)
- [3.4 How to obsidian](#how-to-obsidian)
- [3.5 Security](#security)

# 1. Introduction
>This project is a website for the carnaval's organisation "De Stokers".
>It is meant to attract more members to the organisation and to plan and see all upcoming activities that they are going to partake in. Plus you can see pictures and videos of previous activities and specials like the "Mooi man" cover and a caranval press conference.
>
>The project uses a react frontend and a asp.net API that manages the activities.
>Furthermore it uses the instagram and YouTube API to show the stokers instagram feed and its YouTube specials.

# 2. Learning outcomes
## 1-FullStack
- _"You design and build **user-friendly**, **full-stack** web applications."_

>For my website I designed a frontend that looks like this:
![image](https://user-images.githubusercontent.com/73878099/173580473-793f520f-2152-4583-8eb5-1c19c9bfd9b3.png)
>
>Furthermore it can show you all the upcomming activities:
![image](https://user-images.githubusercontent.com/73878099/173631371-43c77552-1168-410f-9ff5-b87ced6dd071.png)
>
>You can also see the stokers specials on the website:
![image](https://user-images.githubusercontent.com/73878099/173631594-dffdddd3-4290-409a-8ad4-2457a92fdae5.png)
>
>Plus you can login using Auth0:
>
>![image](https://user-images.githubusercontent.com/73878099/173632445-2d1441bf-ae08-4416-a414-1bb82c13588c.png)
>
>I made this using React JS because I had never used Javascript and I would love to learn it since it is growing in popularity and it seemed to be handy in the future.

[Back to table of contents](#table-of-contents)

## 2-Tooling
- _You use software **tooling and methodology** that continuously monitors and improve the software quality during software development._

>To complete this I used Sonarcloud, This checked my code each time I pushed something to git. I chose for this type of static code analysis since I usually create "Messy" code.
>
>![[image]](https://github.com/StokersWebsite/.github/blob/e0bd499b9bc15a84ee4a9c0c9c5e085e1f7ff7a8/Images/Sonarcloud%20overview.png)
>![[image]](https://github.com/StokersWebsite/.github/blob/e0bd499b9bc15a84ee4a9c0c9c5e085e1f7ff7a8/Images/Sonarcloud%20outcomes.png)
 I dont always remove my commented code that I am not going to use. And import things that I then dont use. This way I could easily find those things to clean up my code. 
>![[image]](https://github.com/StokersWebsite/.github/blob/e0bd499b9bc15a84ee4a9c0c9c5e085e1f7ff7a8/Images/Sonarcloud%20Quality%20gate.png)
>I also used postman to test if my API was working correctly, here is a demonstration:
>![Postman Demo](https://github.com/StokersWebsite/.github/blob/594875f9ec52fb7b295ea3c71fe8390a96cf5e01/Images/PostmanDemo.gif)
>Sonarcloud also mentions some Security hotspots but those are neglectable since I need that to make my API publically available.
>### Eeventify
>For the group project we also made integration tests, We felt like this was the most usefull test since then we could see if everybody's code could work together.
>![[image]](https://github.com/StokersWebsite/.github/blob/e0bd499b9bc15a84ee4a9c0c9c5e085e1f7ff7a8/Images/eeventify_postman_test.png)
>And we monitored the status of the application, We did this because the application runs on a group members home server and this way we could check if it was still working.
>![[image]](https://github.com/StokersWebsite/.github/blob/e0bd499b9bc15a84ee4a9c0c9c5e085e1f7ff7a8/Images/eeventify_postman_monitor.png)

[Back to table of contents](#table-of-contents)

## 3-Agile
- _You **choose** and implement the most suitable agile software development method for your software project._

>For the group project we used Scrum as our [[Agile]] method. We did this using Taiga. This is a program that allows you to make a board per sprint that has all tasks which you can assign to people. We chose scrum since the finnish students had used this method before and would like to do it again. We used taiga as our scrum software and had a taiga project for the front-and-back end so we could see each others progress. 
>
>![[image]](https://github.com/StokersWebsite/.github/blob/11ec8d6b4546d83171fa616700d5d053ab0ffb10/Images/Taiga%20Board%202.png)
>![[image]](https://github.com/StokersWebsite/.github/blob/078f45a6748fc5ed25ffdb03fc0781c31c266170/Images/Sprint%204%20completed.png)

[Back to table of contents](#table-of-contents)

## 4-CiCd
- _You **design and implement** a (semi)automated software release process that matches the needs of the project context._

>I used github actions to create a CI/CD pipeline. So everyime I pushed something to github it would check the code and then deploy it on docker. I felt this was the most educational and do-able, since I was already using github it made the most sense to use this as my CI/CD method since I could check it and deploy it everytime I updated my code, while not changing my codes location.
![[image]](https://github.com/StokersWebsite/.github/blob/f237d7180f1d9e2dd15e4b0b298508afa0b6a7ee/Images/DockerRunning.png)
![[image]](https://github.com/StokersWebsite/.github/blob/11ec8d6b4546d83171fa616700d5d053ab0ffb10/Images/GithubActions.png)

[Back to table of contents](#table-of-contents)

## 5-Cultural diffrences
- _You **recognize** and **take into account** cultural differences between project stakeholders and ethical aspects in software development._

>### Finland
>For me the cultural differences were very visable since I worked on the Oulu project with finnish students. I feel like that we as dutch students inherited a lot of the finnish ways of doing things. Like taiga, We had all never heard of it, but since the finnish students had and liked it we decided to use it for this project aswell.
>
>### Ethics
>For [[Ethics]] we had to think of ways that our application might affect its users.
Our group application is a social media application, As such our users would be able to chat with each other. This in and of itself could be problematic since it could be used to insult other people. Our application is also based on group activities, this means users could exclude other users from a certain activity, this would [inflict harm](https://www.acm.org/code-of-ethics#:~:text=locally%20and%20globally.-,1.2%20Avoid%20harm.,-In%20this%20document) to other users using our software.

[Back to table of contents](#table-of-contents)

## 6-Requirements
- _You analyze (non-functional) requirements, elaborate (architectural) designs and validate them using **multiple types of test techniques**._

>### teachers
>I had multiple stakeholders including my teachers, cv de stokers members and myself.
For the "user acceptance" of the teachers I ofcourse had feedback moments and casual conversations (with leon) about my project and progress. I did this because then I got to know more about what still had to be done. And I got some good tips on how to move forward.
>![[image]](https://github.com/StokersWebsite/.github/blob/e0bd499b9bc15a84ee4a9c0c9c5e085e1f7ff7a8/Images/Feedpulse.png)
>### Stokers members
>I also got feedback as user acceptance testing from Stokers members, first of all about the requirements ofcourse. I did this at the start because I wanted to know what all the members wanted in the site. 
From this I learned that most members would like a activities tab on which they can see what events are comming up, which I then added to the requirements.
>![[image]](https://github.com/StokersWebsite/.github/blob/e0bd499b9bc15a84ee4a9c0c9c5e085e1f7ff7a8/Images/Activity%20requirements.png)
>### Sonarcloud
>To check my code quality I used sonarcloud
>![[image]](https://github.com/StokersWebsite/.github/blob/e0bd499b9bc15a84ee4a9c0c9c5e085e1f7ff7a8/Images/Sonarcloud%20Outcomes2.png)
>![[image]](https://github.com/StokersWebsite/.github/blob/e0bd499b9bc15a84ee4a9c0c9c5e085e1f7ff7a8/Images/Sonarcloud%20findings.png)
>I used sonarcloud because then I could find everything that was not neat code easily.
For example if I imported something that I didnt use it would show me in what file I did so.
This came in very handy to clean up my code.
>### Eeventify
>for the group project we planned everything out way better than for my personal project, for example by making a architecture diagram:
>![image](https://github.com/StokersWebsite/.github/blob/bfdb67662045b1986345ef1bd5f140006d0e8c87/Images/unknown.png)

[Back to table of contents](#table-of-contents)

## 7-Business process
- _You analyze and describe **simple** business processes that are **related** to your project._

[Back to table of contents](#table-of-contents)

## 8-Professional
- _You act in a **professional manner** during software development and learning._

>For me this was both the easiest and the hardest to prove. I felt like everything I did this semester like the group project, my feedback usage and my on logical thinking based decisions proved that I acted in a professional manner. Even so I was never really sure if this was the way to show this.
>
>![[image]](https://github.com/StokersWebsite/.github/blob/e0bd499b9bc15a84ee4a9c0c9c5e085e1f7ff7a8/Images/Feedpulse.png)

[Back to table of contents](#table-of-contents)

# 3. Research
As of research i did for this semester:
## Ethics in software 
>As in most things ethics also apply when creating software. You may think ethics arent a big  deal in software development, but you would be mistaken.
There are a lot of choises when developing software based on ethical and moral choises. To see my full ethics research:
>
>[[📄Ethics research]](https://github.com/StokersWebsite/.github/blob/31c1068a435684bf41054adccb10a86c87268d3d/Research/Ethics.md)

## Agile Methods
>There are more than one correct agile methods that you can use for a group project. We chose for Scum, to learn more about scrum and other agile methods:
>
>[[📄Agile]](https://github.com/StokersWebsite/.github/blob/31c1068a435684bf41054adccb10a86c87268d3d/Research/Agile.md)

## How to obsidian
>For my personal research this semester I chose "How to obsidian". My teacher recommended that I start using obsidian, and so I did. 
>I liked it so much that I wanted to do my research about it too. 
>To check that out:
>
>[[📄 How to Obsidian]](https://github.com/StokersWebsite/.github/blob/31c1068a435684bf41054adccb10a86c87268d3d/Research/Obsidian.md)

## Security
>This semester I also learned a lot about security, And especially on what to do about security for specific types of project. This is why my security research is (primarily) about what my project needed for security.
>To see this:
>
>[[📄 My Security]](https://github.com/StokersWebsite/.github/blob/31c1068a435684bf41054adccb10a86c87268d3d/Research/Security.md)

[Back to table of contents](#table-of-contents)
