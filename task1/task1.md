# Task 1: Networks

## Outline

In this task, we try to explore how the Internet works. There are a few subtasks that require programming. That is to say, you'd better create a GitHub repo. The commit messages should strictly follow the [Angular Commit Format](https://gist.github.com/brianclements/841ea7bffdb01346392c).

## Prerequisites & Resources 

- Learn how to use Libgen for free e-books. Download the book "Computer Networks - A Top-Down Approach". Read the chapter "Application Layer" as well as the ipv4 part in the chapter "Network Layer".  
- [Python](https://docs.python.org/3/tutorial/index.html) (To learn a new language, I recommend skimming through the basic syntax first, then just use it! If you encounter any obstacles in your work, go back and only read what you need.)
- [URL](https://en.wikipedia.org/wiki/URL)
- [URL encoding](https://en.wikipedia.org/wiki/URL_encoding)
- [base64](https://en.wikipedia.org/wiki/Base64)
- [Docker](https://docker-curriculum.com/)

Upon Finishing, try ask yourself a few questions to get prepared.  

- What is 0.0.0.0, 127.0.0.1, 192.168.1.1, 255.255.255.255, 192.168.1.255?
- How to capture packets?
- How does a VPN work?

## Procedure & Criteria

### Written Part

For the following subtasks, create a markdown file, and write your answer into it. DO NOT only give the final answer without any explanations or detailed steps.

1. What is your private ip and public ip? (5 pts)

2. What is the ip address of hust.edu.cn? (5 pts)

3. How many hops are there between your host and example.com? (5 pts)

4. [Here](./attachment0) is a mail message, what is the sender's ip address? (5 pts)

5. Try to trace an iterative DNS query, what is the ip of the root server, the tld server, and the authoritative server respectively? (5 pts)

6. There is a tcp server listening on port 3000. It holds a secret pincode, a.k.a. a four-digit number. You can send any messages to it, and it only responds 'y' when the message you send is the right pincode. Otherwise, it responds 'n'.  
You can pull the docker image of the server [here](https://hub.docker.com/repository/docker/lesliejiang/pincode/general), and run it on your local machine.  
What is the right pincode? (10 pts)

7. There is a http server (That is to say, you can visit it in your browser) listening on port 5000. If you visit it directly, you'll get blocked. Try bypassing its limitations. After that, you'll see a string like "flag{ xxxx }", which we call a flag. Likewise, [here](https://hub.docker.com/repository/docker/lesliejiang/header/general) is the docker image.  
What is the flag? (10 pts)

8. There is a http server listening on port 5000. Try to bypass the login, then you'll see the flag. The docker image is [here](https://hub.docker.com/repository/docker/lesliejiang/cookies/general).  
What is the flag? (20 pts)  
*This task is a bit harder than the others, you can see the tips below first. If you're still confused, try some hints! ([hint0](./hint0), [hint1](./hint1), [hint2](./hint2)) But your score will be reduced by 5 for each hint you use.*  
> Tips: Have you ever wondered why you don't need to login when you visit a website for a second time?

### Coding Part

1. Write a program to test whether you're in a VPN environment. (You can test whether it is correct by switching on and off your vpn and see the output) (10 pts)
```bash
$ vpn-detect
True
```
(Language does not matter.)
```bash
$ python3 vpn-detect.py
False
```
> Tips: Do you know your public ip? There're multiple ways to get an answer.

2. Implement a BitTorrent client.  
In fact, there is already a half-done one. See this [repo](https://github.com/eliasson/pieces/) as well as the relevant [article](https://markuseliasson.se/article/bittorrent-in-python/).  
After reading through the article, you'll find that seeding is not yet implemented. So what you need to do is quite simple: implement seeding (which means uploading pieces). (25 pts)
> Tips: Don't start from zero. Just clone the repo and build your codebase upon it. Also, since it is quite a lot of work, let AIs generate codes for you, especially Copilot and Codeium.