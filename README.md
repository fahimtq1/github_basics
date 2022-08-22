# Git and GitHub basics

You can see my [video tutorial](https://testingcircle-my.sharepoint.com/:v:/g/personal/fqurashi_spartaglobal_com/ESVqrtVkHzZLnZ2j3sXa3ncBNPMjiM_5adSBBEUSZzPfqw

## What is GitHub?

GitHub is a website (global host) that hosts Git repositories. There are other remote hosts like GitHub, but GitHub is free to use and the most popular.

### How to set up GitHub?

An account is required for GitHub, therefore you need to sign up with an email and set a password on the [GitHub website](https://github.com/). A confirmation email will be sent to verify the email address that you have inputted. After following the relevant steps, you GitHub account will be available to use as a remote host for your repositories!

![image](https://user-images.githubusercontent.com/99980305/182087513-8df9096b-f1b1-4ddb-947e-98f81e3ccb47.png)

## What is Git?

Git is a free and open-source Version Control System (VCS). A VCS is software that manages the changes to documents, computer programs and other collections of information. This way, an individual can track all the changes made to a file, as well as view the version history of that file. 

### How to set up Git?

If you are using MAC OS or Linux, then these operating systems tend to have Git pre-installed. If you are a Windows user, you can download Git here on [Git Bash](https://git-scm.com/download/win). Git Bash will be your Git terminal.

![image](https://user-images.githubusercontent.com/99980305/182088191-8d613443-0a33-4d72-827a-67ad58beaa3c.png)

### Basic Git and Linux commands

Specific Git commands are formatted in the following way, ```git (insert command here)```, and in this section I will detail a few basic Git commands. You will also need a know a few Linux commands to navigate your local host's files.

#### Git commands:

- ```clone```: a repository hosted on GitHub is brought into a directory on the local host
- ```add```: tracks files and changes in Git
- ```commit```: saves files and changes in Git
- ```push```: uploads Git commits to a remote repository on a global host like GitHub
- ```status```: shows all the changes that haven't beem committed
- ```cat```: displays the contents of a file without opening the file
- ```nano```: opens a new window to allow the editing of a file

#### Linux commands:

- ```cd```: change directory to a name inserted after, or if a ".." is placed, the directory goes backward one step
- ```ls```: lists all the files in the current directory
- ```ls -la```: shows all files, including hidden files
- ```pwd```: prints working directory
- ```clear```: clears the terminal entries
- ```mkdir```: makes a directory
- ```rm -rf```: deletes a file/folder

## Linking Git and GitHub:

In order to link Git on your local host and GitHub there are two methdos: clone with HTTPS or clone with SSH keys. To download a repository you must first make a repository on GitHub by navigating to the repositories page and then clicking on "New."

### HTTPS

This method is quick and easy. You must access the the code on your repository with a HTTPS link using the following button:

![image](https://user-images.githubusercontent.com/99980305/182091461-1231d393-7956-41c8-b807-a3e2e3ec85b3.png)

Before you paste the link in your chosen command line interface, ensure it will be cloned into the correct repository- this can be confirmed using the cd and mkdir Linux commands. You then paste the link into your terminal like this: ```git clone (paste link)```. Your remote repository has now been downloaded onto your local host. 

### SSH keys:

Another method, to download a GitHub repository onto your local host, is by using SSH keys. The command to generate keys is: ```ssh-keygen -t rsa -b 4096 -C "(insert your GitHub email"```. This generates two keys: a public key and a private key. 

The private key has to remain secure and the public key is uploaded to the GitHub interface. If you are to "push", then the private key shows GitHub that you are the owner of the public key that it has, therefore it allows the "push" to proceed. 

The public key can be pasted by going to the settings page and then to this section:

![image](https://user-images.githubusercontent.com/99980305/182094954-a00d8f4c-4b08-4e3b-9a67-c10806517b52.png)

Finally, to ensure that your local Git command line knows about the generated key, follow these steps:

![ssh keys](https://user-images.githubusercontent.com/99980305/182096165-d7781875-c166-4aae-bc1c-3af811658218.png)

### git push 

Once you have downloaded content, you can make changes to the files and then use ```git status``` to see any changes. Next, use ```git add``` and ```git commit``` to track and save those changes. Finally, use ```git push -u origin main``` to push to the main branch on your remote repository. 

If you have started on a local host, first you need to initialise the repository into a git repository using ```git init```. Then once you are ready to upload onto GitHub, you need to make a reference to the remote repository that you wish to push to. This is done with ```git remote add origin (paste SSH or HTTPS)```. You can now complete this process with '''git push -u origin main'''.

## Summary:

The following diagram demonstrates a summary of the interaction between Git on your localhost and Github:

![git_diagram](https://user-images.githubusercontent.com/99980305/182149272-5e880803-e755-48ba-a644-63ac2fb87525.png)

