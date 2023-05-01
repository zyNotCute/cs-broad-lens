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

- What is your private ip and public ip?
- What is 0.0.0.0, 127.0.0.1, 192.168.1.1, 255.255.255.255, 192.168.1.255?
- Try an iterative DNS query, what is the ip of the root server, the tld server, and the authoritative server respectively?
- How to capture packets?
- How VPN works?

## Procedure & Criteria

### Written Part

For the following subtasks, create a markdown file, and write your answer into it. DO NOT only give the final answer without any explanations or detailed steps.

1. What is the ip address of hust.edu.cn? (5 pts)
2. [Here](./attachment0) is a mail message, what is the sender's ip address? (5 pts)
3. I set up a tcp server listening on port 3000. It holds a secret pincode, a.k.a. a four-digit number. You can send any messages to it, and it only responds 'y' when the message you send is the right pincode. Otherwise, it responds 'n'.  
You can pull the docker image of the server [here](https://hub.docker.com/repository/docker/lesliejiang/pincode/general), and run it on your local machine.  
Your goal is to find the right pincode. (10 pts)
4. I set up a http server (That is to say, you can see it in your browser) listening on port 5000. If you visit it directly, you'll get blocked. Try escaping its limitations. Likewise, [here](https://hub.docker.com/repository/docker/lesliejiang/header/general) is the docker image.
Your goal is to get the original content of that web page. (10 pts)

### Coding Part

1. Write a program to test whether you're in a VPN environment. (10 pts)
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
