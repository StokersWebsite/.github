![image](https://user-images.githubusercontent.com/73878099/172373718-1e27b565-88ea-44ab-bbdc-255b3256cc2f.png)

># Stokers Portfolio
By: Rens Vlooswijk
For: Cv De Stokers and Fontys Semester 3

# Table of Contents:
### 1. Introduction
### 2. Learning outcomes
2.1 FullStack
2.2 Tooling
2.3 Agile
2.4 CI/CD
2.5 Cultural Diffrences
2.6  Requirements
2.7 Business process
2.8 Professional

### 3. Research
3.1 Ethics
3.2 Cultural Differences
3.3 Agile methods
3.4 How to obsidian
3.5 Security

# 1. Introduction
>This project is a website for the carnaval's organisation "De Stokers".
>It is meant to attract more members to the organisation and to plan and see all upcoming activities that they are going to partake in. Plus you can see pictures and videos of previous activities and specials like the "Mooi man" cover and a caranval press conference.
>
>The project uses a react frontend and a asp.net API that manages the activities.
>Furthermore it uses the instagram and YouTube API to show the stokers instagram feed and its YouTube specials.

# 2. Learning outcomes
## 1-FullStack
- _"You design and build **user-friendly**, **full-stack** web applications."_

>## For my website I designed a frontend that looks like this:
![image](https://user-images.githubusercontent.com/73878099/173580473-793f520f-2152-4583-8eb5-1c19c9bfd9b3.png)
>## Furthermore it can show you all the upcomming activities:
![image](https://user-images.githubusercontent.com/73878099/173631371-43c77552-1168-410f-9ff5-b87ced6dd071.png)
>## You can also see the stokers specials on the website:
![image](https://user-images.githubusercontent.com/73878099/173631594-dffdddd3-4290-409a-8ad4-2457a92fdae5.png)
>## Plus you can login using Auth0:
![image](https://user-images.githubusercontent.com/73878099/173632445-2d1441bf-ae08-4416-a414-1bb82c13588c.png)
>I made this using React JS because I had never used Javascript and I would love to learn it since it is growing in popularity and it seemed to be handy in the future.

## 2-Tooling
- _You use software **tooling and methodology** that continuously monitors and improve the software quality during software development._

>To complete this I used Sonarcloud, This checked my code each time I pushed something to git. I chose for this type of static code analysis since I usually create "Messy" code.
>
>![[image]](https://github.com/StokersWebsite/.github/blob/e0bd499b9bc15a84ee4a9c0c9c5e085e1f7ff7a8/Images/Sonarcloud%20overview.png)
>![[image]](https://github.com/StokersWebsite/.github/blob/e0bd499b9bc15a84ee4a9c0c9c5e085e1f7ff7a8/Images/Sonarcloud%20outcomes.png)
 I dont always remove my commented code that I am not going to use. And import things that I then dont use. This way I could easily find those things to clean up my code. 
>![[image]](https://github.com/StokersWebsite/.github/blob/e0bd499b9bc15a84ee4a9c0c9c5e085e1f7ff7a8/Images/Sonarcloud%20Quality%20gate.png)
Sonarcloud also mentions some Security hotspots but those are neglectable since I need that to make my API publically available.
>### Eeventify
>For the group project we also made integration tests, We felt like this was the most usefull test since then we could see if everybody's code could work together.
>![[image]](https://github.com/StokersWebsite/.github/blob/e0bd499b9bc15a84ee4a9c0c9c5e085e1f7ff7a8/Images/eeventify_postman_test.png)
>And we monitored the status of the application, We did this because the application runs on a group members home server and this way we could check if it was still working.
>![[image]](https://github.com/StokersWebsite/.github/blob/e0bd499b9bc15a84ee4a9c0c9c5e085e1f7ff7a8/Images/eeventify_postman_monitor.png)

## 3-Agile
- _You **choose** and implement the most suitable agile software development method for your software project._

>For the group project we used Scrum as our [[Agile]] method. We did this using Taiga. This is a program that allows you to make a board per sprint that has all tasks which you can assign to people. We chose scrum since the finnish students had used this method before and would like to do it again. We used taiga as our scrum software and had a taiga project for the front-and-back end so we could see each others progress. 
>
>![[image]](https://github.com/StokersWebsite/.github/blob/11ec8d6b4546d83171fa616700d5d053ab0ffb10/Images/Taiga%20Board%202.png)
>![[image]](https://github.com/StokersWebsite/.github/blob/078f45a6748fc5ed25ffdb03fc0781c31c266170/Images/Sprint%204%20completed.png)

## 4-CiCd
- _You **design and implement** a (semi)automated software release process that matches the needs of the project context._

>I used github actions to create a CI/CD pipeline. So everyime I pushed something to github it would check the code and then deploy it on docker. I felt this was the most educational and do-able, since I was already using github it made the most sense to use this as my CI/CD method since I could check it and deploy it everytime I updated my code, while not changing my codes location.
![[image]](https://github.com/StokersWebsite/.github/blob/f237d7180f1d9e2dd15e4b0b298508afa0b6a7ee/Images/DockerRunning.png)
![[image]](https://github.com/StokersWebsite/.github/blob/11ec8d6b4546d83171fa616700d5d053ab0ffb10/Images/GithubActions.png)

## 5-Cultural diffrences
- _You **recognize** and **take into account** cultural differences between project stakeholders and ethical aspects in software development._

>### Finland
>For me the cultural differences were very visable since I worked on the Oulu project with finnish students. I feel like that we as dutch students inherited a lot of the finnish ways of doing things. Like taiga, We had all never heard of it, but since the finnish students had and liked it we decided to use it for this project aswell.
>
>### Ethics
>For [[Ethics]] we had to think of ways that our application might affect its users.
Our group application is a social media application, As such our users would be able to chat with each other. This in and of itself could be problematic since it could be used to insult other people. Our application is also based on group activities, this means users could exclude other users from a certain activity, this would [inflict harm](https://www.acm.org/code-of-ethics#:~:text=locally%20and%20globally.-,1.2%20Avoid%20harm.,-In%20this%20document) to other users using our software.

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

## 7-Business process
- _You analyze and describe **simple** business processes that are **related** to your project._

## 8-Professional
- _You act in a **professional manner** during software development and learning._

>For me this was both the easiest and the hardest to prove. I felt like everything I did this semester like the group project, my feedback usage and my on logical thinking based decisions proved that I acted in a professional manner. Even so I was never really sure if this was the way to show this.
>![[image]](https://github.com/StokersWebsite/.github/blob/e0bd499b9bc15a84ee4a9c0c9c5e085e1f7ff7a8/Images/Feedpulse.png)

