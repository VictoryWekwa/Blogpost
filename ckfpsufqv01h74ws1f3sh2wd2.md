## How to Push a file on Github using Git

# Introduction

According to [wiki](https://en.wikipedia.org/wiki/GitHub),
GitHub is a tool that offers the distributed version control and source code management (SCM) functionality of Git, plus its own features. It provides access control and several collaboration features such as bug tracking, feature requests, task management, and wikis for every project.

Git is a tool that helps developers to keep and track changes to their code and projects.

According to the  [git documentation](https://git-scm.com/docs/git) ;

> Git is a free and open source distributed version control system 
    designed to handle everything from small to very large projects with 
     speed and efficiency.

It is important to remember that Git and GitHub are not the same thing.

While Github is a tool that helps developers collaborate by hosting their project on Git repositories so teams and others can contribute. Git is a version control system.
Not only codes can be shared on Github, text files and other file formats can also be shared.


## Why do we need Github

- Github provides a way to store your projects in an online location other than your local machine incase something happens to it.

- A great way to collaborate with other people

- Many open source projects are hosted on Github.

# Getting started

The first step to getting started on github is to create an account.

Create an account  [here](https://github.com)  using an email address

## Creating Repository

After signing up on  [github](https://github.com) , the next step is to create a repository.

Login to your account and click on the  button beside your profile picture or the new button below it.


![2b.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1601494823986/Gt8ha2qP3.jpeg)


Create a repository and give it a name, you will see a box to initialize the repository with a readme. check the box and create a repository.


![2a.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1601494872991/qnEqlq8jE.jpeg)


After successsfully creating a repository, you will see some instructions given by git that looks like the one below

```

   echo "#first_repo" >> 
   README.md
   git init
   git add README.md
   git commit -m "first commit"
   git remote add origin   "https://github.com/yourusername/nameofrepo.git"
   git push -u origin master


``` 






### Download  [git](https://git-scm.com/download/win)

and follow the steps to install.

** Configuring Git**

After installing git the next type is to configure it.

Open the installed git and type the following




```
git config --global username "INPUT YOUR USERNAME"
git config --global user.email "Your email address"

``` 





Remember to input your Github email address and username you signed up with.

### Initializing Git

After configuring your Git, the next step is to initialize Git to a repository
to initialize git, follow the steps below


1. On your computer create a folder
2. Open the folder
3. Right click on the folder and select Git bash here, it takes you to the Git bash 

Run the command 

```
 git init 

you will see "Initialized empty git repository in C:/Users/Your_Username/Desktop/foldername"
```

Wondering what just happeneed?

Try typing **ls**, notice that nothing happens which means there is no files there.

Type in  **ls -a**

Did you see any folder called .git?

That is what the **git init** command does, it creates a folder called **.git**
You won't be using the folder, but without that folder, no git command will be able to work .

### Adding Files

The next step to add your files or folders to the git repository.
First drag and drop your files or folders to the folder you created on your computer.
Run the command  

```
 git add .

or

git add -A
```

### Committing the Added Files

Git commit is a way to save the added file and can be done by using the git commit command with a -m flag.

```
git commit -m "commit message"

```
Your commit message can be anything, it can also be a message explaining what the added files does. Just keep it simple.

### Git log
this command is used to know what the commit history looks like, it shows each commit message that has been done, to close the git log command simply press **q**.

```
git log

```

To see your commit message in one line, simply add the > --oneline 
flag to the git log command, this makes make reading the commit message  clearer and easier.

```
 git log --oneline

```

### git status

This command is used to check the stage of your code or project.

### Pushing Your Files to Github

```
git push origin master

 ```
This command is used to send the code to Github, after typing in the git push command, a prompt appears to enter your github username and password.

# Conclusion

In this article, we were able to understand the meaning of Git and Github. And also the basic commands that is used to push our codes or projects to GitHub.
In addition, using Git and GitHub is an important skill every developer should learn. Pushing your code and projects to GitHub should be an habit.
If you feel you have benefitted from this article, kindly like or comment and also share to other people so that they can benefit as well.

Don't forget to click the subscribe button above, so you get updated on my next blog post.
