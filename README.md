# .github
Intro to Reznick Github 

## WELCOME
This platform's intended use is to share code, project files, and data easily across our lab. This is also a convenient way to track student progress if they were to work on your repository. This repository is reserved *ONLY* for informational guidelines such as how to set up a repository, github ettiquette/tips, and also how to use github. Below is a quick crash course on how to get you started with your repository building. 

For basic github commands, please refer to this [link](https://github.com/Reznick-Lab/.github/blob/main/basic-git-commands.md). 


## Crash Course Into Github: 
Github is used as a cloud-based version control platform that uses Git software. Long story short, this is a way to track any changes to your files, code, and projects which can be helpful to a large team sharing data. Through this platform, we can see other people's scripts, share data easily amongst ourselves, and also monitor undergrad progress. 

Folders on Github are called repositories (repos). Repos can be backed up on the github cloud, but can also be stored locally on your computer using the command "git clone". This command will clone your github repo onto your computer, and you can actually push updates from your cloned repository to your github repo. This can be a convenient way to backup your work, and also share your progress with other people. 

For some more basics on best repository practice, please review this [link](https://docs.github.com/en/repositories/creating-and-managing-repositories/best-practices-for-repositories). 

## Why Use Github? 

Originally, Github is a great tool used for software development. Having a central repository that people can clone into, add onto, and fork updates from has a been a great way to push application development. The concept of github revolves around the idea that remote repositories can be shared and accessed easily amongst collaborators to produce scalable and reproduceable work. So, in many ways, there is a lot of overlap in the workflow of a software developer and a researcher. 

From a research perspective, if you are someone analyzing data and writing scripts for that data, you can use github as a platform to backup some of those files onto a cloud. You can set your repository to private, and quietly track changes. Github can also be a great record keeping platform where you can store lab notes, analysis code, and presentations. After publications, github can be a great way to share your data analysis workflows with other collaborators too. As you already may have experience with, you can find many R packages posted here on github that you can use in your regular work like [ColorMesh](https://github.com/J0vid/Colormesh/blob/master/README.md). 

Besides just personal every day use, github could also be an easy way to showcase work you have done as like a virtual resume that you can link to your web page, LinkedIn, and more. 

[This article](https://pmc.ncbi.nlm.nih.gov/articles/PMC11844616/) also provides some great insight into a group's approach to collaborating on github. 

## To Start

1. Before doing anything, most of us have MacOS, if you have a Mac device then follow these instructions. Otherwise, if you have a Windows device, click this [link](https://git-scm.com/install/windows) so you can follow instructions to download Git onto your computer.

   **Mac Users:**
      - Check to make sure you have homebrew installed. This is a free open-source package manager for macOS and Linux. Think of it             like an "App store" for developers. If you do not have it installed, click [here](https://brew.sh/). Otherwise, skip to the             next step. 
      - Open your terminal, and type out the following code:
         <code class="hljs language-shell">$ brew install git</code>
      - note: brew packages historically takes foreverrrr to download, so do this on a day where you know you won't have to run a lot           of terminal commands that day, and can also keep your computer on until the download completes.
      - Not sure if you have git downloaded already? No problem, try this:
        <code class="hljs language-shell">$ git --version </code>
      - If this returns with nothing, then download git. If it returns with something like this...Then you are all set to move onto the         next step, and can use Git commands from your terminal:
        
```
   (base) Leanns-MacBook-Pro:~ froglord$ git --version git 
   version 2.37.1 (Apple Git-137.1)
```
   
**alternatively you can also use [Github Desktop](https://docs.github.com/en/desktop) or [GLI](https://docs.github.com/en/github-cli), but this guide will only cover using Git commands through the terminal** 
        
3.  Create a new repository. Here is the quick start [documentation](https://docs.github.com/en/repositories/creating-and-managing-repositories/quickstart-for-repositories).

4. As part of good practice, always include a README file with your repository. This is as simple as toggling on the "Add README" part when you initially create the repo.
   
5. Optional, but you can also toggle on .gitignore if you know there are files you don't want git to track like for example sensitive script or information, but largely I don't think you will need this function. Also, be sure to include the license Apache 2.0. This license type is legally robust, and supports open-source software. If your downstream intent is to create open source software other scientists or companies can look at and use, then this license type essentially means that you want your code to be free and open-source.

## SSH Keys 

Background: SSH protocol, is a method of authenticating your identity. SSH keys are essentially an authentication credential that offers you remote access to your repository. This means you can update your repository here on github remotely through your local repositories on software like Rstudio or a text editor using git commands without needing to log in every time. By using an SSH key, it tells your computer this is indeed YOU who is accessing YOUR repo, and YOU are pushing these changes. For more background on SSH Keys click [here](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/about-ssh). 

If this is your first time on github, you will need to create an [SSH key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent). 

Once you've created your SSH Key, add that key onto Github using this [documentation](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)

## Shell Commands and Creating Repositories 

HOORAY! You've made your SSH key, now you're ready clone your repo to your local repository: 

### Some Useful Shell Commands 

Access your terminal, and refer to these shell commands to get to the directory you want to connect to a remote repository:  

- lists folders and files 
```
   $ ls //lists folders and files
```
- change directories
```
   $ cd [folder you want to access] 
```
- print working directory. Use this to check if you are in right folder
```
   user$ pwd //print working directory
```
- went into wrong folder? no problem.. use this shell command to go back a step
```
   user$ cd..
```


  Once you've confirmed that you are in the right folder, following these github commands: 

```
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:Reznick-Lab/.github.git //SSH key
git push -u origin main

```

Then, use command 'git clone "paste link"'. Checkout the preview below to see what your terminal should look like: 
 <pre> 
   <code class="hljs langauage-shell"> 
   (base) ucr-secure-01-fs-10-12-135-176:test froglord$ git clone https://github.com/leann-labra/test.git
   Cloning into 'test'...
   remote: Enumerating objects: 3, done.
   remote: Counting objects: 100% (3/3), done.
   remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
   Receiving objects: 100% (3/3), done.</code>
 </pre>

 There ya go! You've connected your remote repository to your existing local repository! 

 ### Cloning into an empty repository 
If you want to create a new repository for an upcoming project, you'll need to create a directory where your cloned repository will live in. Use the below shell commands from above, but also use this new command below. 

```
   user$ mkdir foldername //use this command to make a new folder, keep repo name the same as the repo you're cloning from github. 
```

mkdir: "make directory" which creates a new folder. 

Want to learn more shell commands that will save you lots more time? Click [here!](https://simon-m-mudd.github.io/NMDM_book/#_commands_that_will_save_you_vast_amounts_of_time)


### Additional information (for funsies) 
  - You may come across a command called <code class="hljs language-shell"> $ git init // git initialize</code>
    this is for repositories that are not yet under git, but are initialized to start tracking changes through git. This is **not** to      be confused with <code class="hljs language-shell"> $ git clone </code>. Cloning a repository is only for repos that have remote        repo configured. Git initialize will still track changes through the git software, but you can not push changes onto github unless      you have a corresponding remote repository attached.

  - This feature does have some advantages though, as you can track version changes on your script using git init if you don't want it      visible on your github page just yet.

  - Okay, so if my repo is not cloned from a remote repository, how is git saving all my versio changes? So, this is the cool part          about Git. There is a hidden .git folder attached to your repo. It is a hidden directory that has all the information stored of         your version changes. You can adjust your settings to view the folder if you want to, but it's best not to touch it so you don't        break anything. 
    
Happy coding!












  








