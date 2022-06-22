# How much security do you need?

## table of contents:
- What types of security are there?
- Why do you need security?
- How to improve security yourself?
- My personal project's security
- When is it too much?

# Security research

## introduction
One of the main points of discusion when starting or making a project is its security. How you secure your project is very important because it can really affect its users if its not done properly. But on the other hand it can take a lot of time to setup security. This is why I did my semester 3 research about how much security do I really need.


## What types of security are there?
There are lots of different ways to help secure your website. First and foremost is a SSL certificate. It is a quick way to encrypt information on your website. If you want to know more about SSL certificates you should check out [Robin van Hoof's research on SSL](https://github.com/FHICT-Ordio/general/blob/main/Portfolio/IP/Research/SSL%20Security%20Research.md).
The next main security item is anti-malware software. Anti-malware software can lots of different things like:
- Web scanning
- Malware detection and removal 
- Web application firewall
- Vulnerability patching
- DDoS protection 
- PCI compliance
Another easy thing you should always do is use Difficult passwords. This may seem obvious but this really can help in protecting your website.
Also try to keep your website up-to-date at all times. This again seems obvious but does actually help.
There are a lot more ways to secure your website but these are the main ones that everybody should always do.

## Why do you need security?
The main reason you need security is to keep hackers and cyber thieves from abusing your software. I also made a research document about ethics in which I explain how you could [abuse software](https://github.com/StokersWebsite/.github/blob/31c1068a435684bf41054adccb10a86c87268d3d/Research/Ethics.md#how-could-you-abuse-software). 
In this is explained that without proper security there are lots of things hackers can do with your software.

![hacker](https://user-images.githubusercontent.com/73878099/174445351-93ddbf81-191c-4bda-90dc-d7b104063963.png)

Furthermore the reasons you need security differ per project. For example a banking application needs a lot of security to keep hackers from stealing money, while social media applications need security to keep users from bullying other users. This is however a different kind of security than what this research is about.

## How to improve security yourself?
As mentioned in the beginning there are lots of ways to improve software security. Those however are more focused on the website hosting. There are also ways to improve security when creating the project for example in its code.
Ways to do this are:
- ### Think of security from the beginning
	If you start your project oblivious to security it will be way harder to implement than when you start from the beginning. It is even better when you think of how you are going to secure your project before writing any code.
- ### Use a security framework
	There are frameworks to increase security, This will most likely be secured a lot better than if you create your own security from scratch.
	It will also add structure and consistancy across the entirety of the group
- ### Set up requirements in advance
	You can make sure the security standards are the same on all parts of the project by establishing the security requirements before you start the project. 
- ### protect the code itself
	Save all the code in a protected repository, this way you can manage everybody that can alter the code and oversee all changes.
- ### Review and test your code constantly
	You can find most of your vulnerabilitys by repeatedly testing your code
	If you can remove them before you launch your code the chances of it getting breached are a lot smaller.

## My personal project's security
As of what I did for my project, First and foremost I used Auth0 as a login service. You can only login to the website if I have already created an account for you. This means Auth0 is in control of the security of the login. 
And since I have protected routes to my add activities page, My website doesnt really need any additional security (for now). If I were to publish this website however it would probably need some more security. The main reason for this is that most servers (on which you can host your website) require a SSL certificate befor they allow you to host your website.

![Auth0](https://user-images.githubusercontent.com/73878099/173632445-2d1441bf-ae08-4416-a414-1bb82c13588c.png)

## When is it too much?
How much security a project needs varies a lot from project to project.
For example a crud application doesnt need a lot or any security since there wont be valuable information on it that can be stolen. Plus it will probably not be used by other people. A big / popular application like the rabobank app for example does need lots of security. This makes sense ofcourse since this application stores important date like bank account numbers. 

	
>#### Sources:
>https://www.websitebuilderexpert.com/building-websites/how-to-secure-a-website/ 
>https://github.com/FHICT-Ordio 
>https://strategynewmedia.com/why-web-security-is-important/#:~:text=Web%20security%20is%20important%20to,networks%2C%20and%20other%20IT%20infrastructures.
