# .github
Intro to Reznick Github 

## WELCOME
This platform's intended use is to share code, project files, and data easily across our lab. This is also a convenient way to track student progress if they were to work on your repository. This repository is reserved *ONLY* for informational guidelines such as how to set up a repository, github ettiquette/tips, and also how to use github. Below is a quick crash course on how to get you started with your repository building. 

For basic github commands, please refer to this [link](https://github.com/Reznick-Lab/.github/blob/main/basic-git-commands.md). 


## Crash Course Into Github: 
Github is used as a version control platform. Long story short, this is a way to track any changes to your files, code, and projects which can be helpful to a large team sharing data. Through this platform, we can see other people's scripts, share data easily amongst ourselves, and also monitor undergrad progress. 

Folders on Github are called repositories (repos). Repos can be backed up on the github cloud, but can also be stored locally on your computer using the command "git clone". This command will clone your github repo onto your computer, and you can actually push updates from your cloned repository to your github repo. This can be a convenient way to backup your work, and also share your progress with other people. 

For some more basics on best repository practice, please review this [link](https://docs.github.com/en/repositories/creating-and-managing-repositories/best-practices-for-repositories). 

## To Start

1. Before doing anything, most of us have MacOS, if you have a Mac device then follow these instructions. Otherwise, if you have Windows, click this [link](https://git-scm.com/install/windows) so you can follow instructions to download Git onto your computer.

   **Mac Users:**
      - Check to make sure you have homebrew installed. This is a free open-source package manager for macOS and Linux. Think of it             like an "App store" for developers. If you do not have it installed, click [here](https://brew.sh/). Otherwise, skip to next            step. 
      - Open your terminal, and type out the following code:
         <code class="hljs language-shell">$ brew install git</code>
      - note: brew historically takes foreverrrr to download, so do this on a day where you know you won't have to run a lot of                 terminal commands that day, and can also keep your computer on until the download completes.
      - Not sure if you have git downloaded already? No problem, try this:
        <code class="hljs language-shell">$ git --version </code>
      - If this returns with nothing, then download git. If it returns with something like this...Then you are all set to move onto the         next step, and can use Git commands from your terminal:
        
   <code class="hljs language-shell">
   (base) Leanns-MacBook-Pro:~ froglord$ git --version git 
   version 2.37.1 (Apple Git-137.1)
   </code>    
      
        
3.  Create a new repository. Here is the quick start [documentation](https://docs.github.com/en/repositories/creating-and-managing-repositories/quickstart-for-repositories).

4. As part of good practice, always include a README file with your repository. This is as simple as toggling on the "Add README" part when you initially create the repo.
   
5. Optional, but you can also toggle on .gitignore if you know there are files you don't want git to track like for example sensitive script or information, but largely I don't think you will need this function. Also, be sure to include the license Apache 2.0. This license type is legally robust, and supports open-source software. If your downstream intent is to create open source software other scientists or companies can look at and use, then this license type essentially means that you want your code to be free and open-source.

## SSH Keys 

Background: SSH protocol, is a method of authenticating your identity. SSH keys are essentially an authentication credential that offers you remote access to your repository. This means you can update your repository here on github remotely through your local repositories on software like Rstudio or a text editor using git commands without needing to log in every time. By using an SSH key, it tells your computer this is indeed YOU who is accessing YOUR repo, and YOU are pushing these changes. For more background on SSH Keys click [here](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/about-ssh). 

If this is your first time on github, you will need to create an [SSH key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent). 

Once you've created your SSH Key, add that key onto Github using this [documentation](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)

## Cloning your repository 

HOORAY! You've made your SSH key, now you're ready clone your repo to your local repository: 

### Cloning into an existing Repository: 
Access your terminal, and use this code:  

<pre> <code class="hljs language-shell">
   user$ ls //lists folders/files 
   user$ cd [folder you want to access] //change directory 
   user$ pwd //print working directory-> use to check if you are in right folder. 
</code></pre>

  Once you've confirmed that you are in the right folder, copy the HTTPS link from your github repo (refer to image below). 
  
  <img width="926" height="694" alt="image" src="https://github.com/user-attachments/assets/d535a3a6-324e-4503-a6d9-bbf2ee73dfe5" />)

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

 There ya go! You've connected your remote repository to your existing repository! 

 ### Cloning into an empty repository 
If you want to create a new repository for an upcoming project, use the same commands from above but use this new command below. 

<pre><code class="hljs language-shell">
   user$ mkdir "Folder Name" //use this command to make a new folder, keep repo name the same as the repo you're cloning from github. 
</code></pre>

mkdir: "make directory" which creates a new folder. 

Happy coding! 











  








