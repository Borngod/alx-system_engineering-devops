# 0x09. Web infrastructure design

DevOpsSysAdminweb infrastructure

- By: Sylvain Kalache, co-founder at Holberton School
- Weight: 1
- Project to be done in teams of 3 people (your team: Bernard Appiah, Kuuku Buabeng, James Aidoo)
- Project will start May 25, 2023 6:00 AM, must end by May 29, 2023 6:00 AM
- **Manual QA review must be done** (request it when you are done with the project)

### Concepts

_For this project, we expect you to look at these concepts:_

- [DNS](https://intranet.alxswe.com/concepts/12)
- [Monitoring](https://intranet.alxswe.com/concepts/13)
- [Web Server](https://intranet.alxswe.com/concepts/17)
- [Network basics](https://intranet.alxswe.com/concepts/33)
- [Load balancer](https://intranet.alxswe.com/concepts/46)
- [Server](https://intranet.alxswe.com/concepts/67)

## Resources

**Read or watch**:

- **Network basics** concept page
- **Server** concept page
- **Web server** concept page
- **DNS** concept page
- **Load balancer** concept page
- **Monitoring** concept page
- [What is a database](https://intranet.alxswe.com/rltoken/n3CdS3EA5l5psDDKbEhApA "What is a database")
- [What’s the difference between a web server and an app server?](https://intranet.alxswe.com/rltoken/0as4wDlFqyhLhf0f_gedcw "What's the difference between a web server and an app server?")
- [DNS record types](https://intranet.alxswe.com/rltoken/Pl3UoEfAO7K_jUKRLMmnAQ "DNS record types")
- [Single point of failure](https://intranet.alxswe.com/rltoken/uxpx2YhXs10TFLIDg78chA "Single point of failure")
- [How to avoid downtime when deploying new code](https://intranet.alxswe.com/rltoken/4ansLu2gtHnoFrNThqyObA "How to avoid downtime when deploying new code")
- [High availability cluster (active-active/active-passive)](https://intranet.alxswe.com/rltoken/TAJeVYy9U9iLaEDd6XkbRA "High availability cluster (active-active/active-passive)")
- [What is HTTPS](https://intranet.alxswe.com/rltoken/c0zs2MxrmxFLsCPOizxq6g "What is HTTPS")
- [What is a firewall](https://intranet.alxswe.com/rltoken/j6idMcUTyNEDj1oYDQFmUw "What is a firewall")

## Learning Objectives

At the end of this project, you are expected to be able to [explain to anyone](https://intranet.alxswe.com/rltoken/FPJvEE-DRJDvmVTNWeFR8A "explain to anyone"), **without the help of Google**:

### General

- You must be able to draw a diagram covering the web stack you built with the sysadmin/devops track projects
- You must be able to explain what each component is doing
- You must be able to explain system redundancy
- Know all the mentioned acronyms: LAMP, SPOF, QPS

### Copyright - Plagiarism

- You are tasked to come up with solutions for the tasks below yourself to meet with the above learning objectives.
- You will not be able to meet the objectives of this or any following project by copying and pasting someone else’s work.
- You are not allowed to publish any content of this project.
- Any form of plagiarism is strictly forbidden and will result in removal from the program.

## Requirements

### General

- A `README.md` file, at the root of the folder of the project, is mandatory
- For each task, once you are done whiteboarding (on a whiteboard, piece of paper or software or your choice), take a picture/screenshot of your diagram
- This project will be manually reviewed:
- As each task is completed, the name of that task will turn green
- Upload a screenshot, showing that you completed the required levels, to any image hosting service (I personally use [imgur](https://intranet.alxswe.com/rltoken/m_O2HLsKrO1zg31LMcLOGQ "imgur") but feel free to use anything you want).
- For the following tasks, insert the link from of your screenshot into the answer file
- After pushing your answer file to GitHub, insert the GitHub file link into the URL box
- You will also have to whiteboard each task in front of a mentor, staff or student - no computer or notes will be allowed during the whiteboarding session
- Focus on what you are being asked:
- Cover what the requirements mention, we will explore details in a later project
- Keep in mind that you will have 30 minutes to perform the exercise, you will get points for what is asked in requirements
- Similarly in a job interview, you should answer what the interviewer asked for, be careful about being too verbose - always ask the interviewer if going into details is necessary - speaking too much can play against you
- In this project, again, avoid going in details if not asked

### Quiz questions

**Great!** You've completed the quiz successfully! Keep going! (Show quiz)

#### Question #0

What is a database?

- Is a collection of information that is stored on a physical server and organized so that it can be easily accessed, updated and managed.
    
- Is a collection of information that is stored and organized so that it can be easily accessed, updated and managed.
    
- Is a collection of text files that are stored so that it can be easily accessed, updated and managed by the local application.
    

#### Question #1

What is HTTPS?

- A version of HTTP that protect your personal information.
    
- A version of HTTP that secure the traffic between your browser and the website by encrypting it.
    
- A faster version of HTTP.
    

#### Question #2

What is a DNS?

- A system to translate domain names into IP addresses.
    
- A system that contain all Internet IPs.
    
- A list of domain names.
    

#### Question #3

What is a web server?

- A web server is a software that serves web pages to clients upon their request, it does this over the protocol HTTP.
    
- A web server is a software that serves web pages to clients upon their request.
    
- A web server is a software or physical device serving web pages over HTTP.
    

#### Question #4

What is a codebase?

- Is the collection of source code that is used to build a software system.
    
- Is the most important files of a software system.
    
- A list of software libraries.
    

#### Question #5

What is a server?

- A server is a software that serves web pages.
    
- A server is returning information to other computers when asked.
    
- A server is a device, a virtual device or computer program or providing functionality for other programs or devices, called “clients”.
    

#### Question #6

What is TCP/IP?

- Transmission Control Protocol/Internet Protocol, is a suite of communications protocols used to interconnect network devices on the Internet.
    
- Transmission Control Protocol/Internet Protocol, is a suite of communications protocols used to interconnect network devices on private network.
    
- Transmission Control Protocol/Internet Protocol, is a suite of communications protocols used to interconnect network devices on the Internet or any private network.
    

## Tasks

### 0\. Simple web stack

mandatory

A lot of websites are powered by simple web infrastructure, a lot of time it is composed of a single server with a [LAMP stack](https://intranet.alxswe.com/rltoken/YVDX0XsC6XHp0nmezvT9vQ "LAMP stack").

On a whiteboard, design a one server web infrastructure that hosts the website that is reachable via `www.foobar.com`. Start your explanation by having a user wanting to access your website.

Requirements:

- You must use:
    - 1 server
    - 1 web server (Nginx)
    - 1 application server
    - 1 application files (your code base)
    - 1 database (MySQL)
    - 1 domain name `foobar.com` configured with a `www` record that points to your server IP `8.8.8.8`
- You must be able to explain some specifics about this infrastructure:
    - What is a server
    - What is the role of the domain name
    - What type of DNS record `www` is in `www.foobar.com`
    - What is the role of the web server
    - What is the role of the application server
    - What is the role of the database
    - What is the server using to communicate with the computer of the user requesting the website
- You must be able to explain what the issues are with this infrastructure:
    - SPOF
    - Downtime when maintenance needed (like deploying new code web server needs to be restarted)
    - Cannot scale if too much incoming traffic

Please, remember that everything must be written in English to further your technical ability in a variety of settings.

#### Add URLs here:

 Save 

**Repo:**

- GitHub repository: `alx-system_engineering-devops`
- Directory: `0x09-web_infrastructure_design`
- File: `0-simple_web_stack`

Done?! Help

×

#### Learners who are done with "0. Simple web stack"

### 1\. Distributed web infrastructure

mandatory

On a whiteboard, design a three server web infrastructure that hosts the website `www.foobar.com`.

Requirements:

- You must add:
    - 2 servers
    - 1 web server (Nginx)
    - 1 application server
    - 1 load-balancer (HAproxy)
    - 1 set of application files (your code base)
    - 1 database (MySQL)
- You must be able to explain some specifics about this infrastructure:
    - For every additional element, why you are adding it
    - What distribution algorithm your load balancer is configured with and how it works
    - Is your load-balancer enabling an Active-Active or Active-Passive setup, explain the difference between both
    - How a database Primary-Replica (Master-Slave) cluster works
    - What is the difference between the Primary node and the Replica node in regard to the application
- You must be able to explain what the issues are with this infrastructure:
    - Where are SPOF
    - Security issues (no firewall, no HTTPS)
    - No monitoring

Please, remember that everything must be written in English to further your technical ability in a variety of settings.

#### Add URLs here:

 Save 

**Repo:**

- GitHub repository: `alx-system_engineering-devops`
- Directory: `0x09-web_infrastructure_design`
- File: `1-distributed_web_infrastructure`

Done?! Help

×

#### Learners who are done with "1. Distributed web infrastructure"

### 2\. Secured and monitored web infrastructure

mandatory

On a whiteboard, design a three server web infrastructure that hosts the website `www.foobar.com`, it must be secured, serve encrypted traffic, and be monitored.

Requirements:

- You must add:
    - 3 firewalls
    - 1 SSL certificate to serve `www.foobar.com` over HTTPS
    - 3 monitoring clients (data collector for Sumologic or other monitoring services)
- You must be able to explain some specifics about this infrastructure:
    - For every additional element, why you are adding it
    - What are firewalls for
    - Why is the traffic served over HTTPS
    - What monitoring is used for
    - How the monitoring tool is collecting data
    - Explain what to do if you want to monitor your web server QPS
- You must be able to explain what the issues are with this infrastructure:
    - Why terminating SSL at the load balancer level is an issue
    - Why having only one MySQL server capable of accepting writes is an issue
    - Why having servers with all the same components (database, web server and application server) might be a problem

Please, remember that everything must be written in English to further your technical ability in a variety of settings.

#### Add URLs here:

 Save 

**Repo:**

- GitHub repository: `alx-system_engineering-devops`
- Directory: `0x09-web_infrastructure_design`
- File: `2-secured_and_monitored_web_infrastructure`

Done?! Help

×

#### Learners who are done with "2. Secured and monitored web infrastructure"

### 3\. Scale up

#advanced

Readme

- [Application server vs web server](https://intranet.alxswe.com/rltoken/toFi_SdFHyi2MaELB8ekqw "Application server vs web server")

Requirements:

- You must add:
    - 1 server
    - 1 load-balancer (HAproxy) configured as cluster with the other one
    - Split components (web server, application server, database) with their own server
- You must be able to explain some specifics about this infrastructure:
    - For every additional element, why you are adding it

Please, remember that everything must be written in English to further your technical ability in a variety of settings.

#### Add URLs here:

 Save 

**Repo:**

- GitHub repository: `alx-system_engineering-devops`
- Directory: `0x09-web_infrastructure_design`
- File: `3-scale_up`
