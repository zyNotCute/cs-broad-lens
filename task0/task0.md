# Task 0: Toolchains

## Outline

In this task, we try to build a half-automated note management system, with the ability of automatically deploying itself to your personal website.  
Afterwards, all your study notes can be placed here.

## Prerequisites & Resources  

- [Markdown](https://www.markdownguide.org/basic-syntax/)   
- [Git (Chapter 2 ~ 3)](https://git-scm.com/book/zh/v2)  
- [Linux (Chapter 3 ~ 6)](https://101.lug.ustc.edu.cn/)  

After reading these materials, you can ask yourself the following questions to get prepared. If you get stucked, just turn to AIs for help.

- How to use a photo as a hyperlink in Markdown?
- What is a relative path? What about an absolute path?
- What is the file system like on Linux?
- What is the difference between a text file and a binary file? For each, how to open it?

## Procedure & Criteria

1. Install hexo. (15 pts)
> keywords: package manager, npm
2. Write some posts and convert them into static webpages. (15 pts)
> keywords: markdown, hexo 
3. Use your favorite theme. (15 pts)
> keywords: git
4. Deploy it to your personal website. (15 pts)
> keywords: github pages, ssh
5. Enable functions below (10 pts + 10pts):
- If you run command:
```bash
note new
```
You'll get a new .md file in your _posts directory, named after the date today. (If it already exists, then ignore) And your editor automatically open, allow you to edit this file.
- And if you run:
```bash
note find <string>
```
You'll get a list of lines which contains the specific string from all your posts, with line numbers and dates annotated by the side.
> keywords: bash
6. Automate the deployment. (20 pts) (There are two ways, try either one.)
- Deploy at startup.
> keywords: system service
- Deploy daily at a fixed time.
> keywords: crontab