# BASIC GITHUB COMMANDS 

In the crash course, I covered some basic command line keywords to access folders, files, and to create new directories. Here I've laid out a table of basic github commands you can use in your terminal to access some basic github features. 

For those of you who are trying to navigate how to create your own README/instructional files, I've found a neat markdown cheatsheet you can access [here](https://www.markdownguide.org/cheat-sheet/)

There are a lot of features of github you can access just straight from the browser. For example, I am not currently using a 3rd party text editor to draft this tutorial. I am directly typing out this tutorial directly into the github editor file which works just fine. Overall, if the program you are using gas a terminal (i.e. R studio), you can git commit changes from there or just from your Mac's terminal in general! 

To gain more control over Git and it's features, it's important to be familiar with some basic comands to perform actions on your local repositories. I will go over some basic commands below, but for more information checkout this awesome page actually deployed through github about [Numeracy, Modelling and Data Management for the Natural Sciences](https://simon-m-mudd.github.io/NMDM_book/#_version_control_with_git). This is a great resource if you plan on integrating Git into more of your projects down the line. 

Here is a great image to explain the mechanics how your Local Repository (or the repo on your computer) and your remote repository on github interact with each other. This will give you a good visual of what the below git commands mean, and how they affect your repositories...

## Github Workflow Diagram 

<img src="https://ourcodingclub.github.io/assets/img/tutorials/git-for-labs/git_cli.png" alt="Git command schematic">
**from https://ourcodingclub.github.io/tutorials/git-for-labs/#organise**

## Github Commands 

Please find below some basic Git commands you can use... 

![github commands](https://substackcdn.com/image/fetch/$s_!vvWo!,w_1456,c_limit,f_webp,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe8a1b87f-c431-48f0-af52-b4f36825841c_811x976.png)


## General Tips to Avoid Potential Errors: 
  1. **Git commit often**. Why? When you have changes that are unstaged, you will encounter errors that will prevent you from being able      to push changes to your local and remote repository. Besides errors, commiting your changes OFTEN logs changes made on your repo         that you can always return to if problems arise downstream. It's so easy to get locked-into a work flow, and you forget to commit        until the very end. The issue with this arises when something happens that may cause you to lose your progress due to hardware           malfuncitons. Without recent and routine git commits, you lose much more progress than you otherwise would if you just routinely         committed changes instead. The best advice for your work flow is to work section by section, 
     ```
     $ git commit -m "message"
     ```
  2. Unsure if you have unstaged commits? Easy: try git status. This is a great way to catch errors before they happen. 
      ```
      $ git status
      ```
  3.  Want to see all the commits you've made? Use this command, to see a log of all your commit messages. For more documentation on git       log, see this [page](https://git-scm.com/docs/git-log). 
      ```
      $ git log 
      ```
  4.  Before pushing changes to your local repository, do a pull request first to make sure that there aren't any merge conflicts. This        is important to avoid rebase errors, which is essentially when errors return on your temrinal when you try to integrate changes          from one branch to another. This is usually a result of there having conflicting histories between your remote repo vs your local        repo.  
  
      ```
      $ git pull origin main
      ```
      ```
      $ git push origin main 
      ```

  5. When working on a collaborative project that requires multiple researchers or students working out of the same repository, create        separate branches. Push changes onto your branch, and then, when ready, you can merge changes onto the main branch. The reason for       this is if errors on one person's code, it doesn't affect the upstream repo that is connected to everyone else's repo. There many        reasons why you would create a branch, sometimes you want to create a branch to delegate work. Other times, you may want to create       a branch to just test run a pipeline without affecting the work you've already done, then merge changes later to your main branch        if it works out. For any reason why you'd want to create a branch, the important thing is to make sure you don't muddy your              upstream branch, or your main branch when using branches! How you do this, is to git pull regularly, commit changes routinely, and       then push changes to main branch when ready. 

     - Shorthand listed below on...
    
     ```
     $ git checkout -b "branch name"
     ```
