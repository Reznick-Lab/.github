# .github
Intro to Reznick Github 

## WELCOME
This platform's intended use is to share code, project files, and data easily across our lab. This is also a convenient way to track student progress if they were to work on your repository.

## Crash Course Into Github: 
Github is used as a version control platform. Long story short, this is a way to track any changes to your files, code, and projects which can be helpful to a large team sharing data. Through this platform, we can see other people's scripts, share data easily amongst ourselves, and also monitor undergrad progress. 

Folders on Github are called repositories (repos). Repos can be backed up on the github cloud, but can also be stored locally on your computer using the command "git clone". This command will clone your github repo onto your computer, and you can actually push updates from your cloned repository to your github repo. This can be a convenient way to backup your work, and also share your progress with other people. 

For some more basics on best repository practice, please review this [link](https://docs.github.com/en/repositories/creating-and-managing-repositories/best-practices-for-repositories). 

### To Start

1. Create a new repository. Here is the quick start [documentation](https://docs.github.com/en/repositories/creating-and-managing-repositories/quickstart-for-repositories).

2. As part of good practice, always include a README file with your repository. This is as simple as toggling on the "Add README" part when you initially create the repo.
   
3. Optional, but you can also toggle on .gitignore if you know there are files you don't want git to track like for example sensitive script or information, but largely I don't think you will need this function. Also, be sure to include the license Apache 2.0. This license type is legally robust, and supports open-source software. If your downstream intent is to create open source software other scientists or companies can look at and use, then this license type essentially means that you want your code to be free and open-source.

## SSH Keys 

Background: SSH protocol, is a method of authenticating your identity. SSH keys are essentially an authentication credential that offers you remote access to your repository. This means you can update your repository here on github remotely through your local repositories on software like Rstudio or a text editor using git commands without needing to log in every time. By using an SSH key, it tells your computer this is indeed YOU who is accessing YOUR repo, and YOU are pushing these changes. For more background on SSH Keys click [here](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/about-ssh). 

If this is your first time on github, you will need to create an [SSH key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent). 

Once you've created your SSH Key, add that key onto Github using this [documentation](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)

## Cloning your repository 

HOORAY! You've made your SSH key, now you're ready clone your repo to your local repository: 

Pre-existing Repository: 
Access your terminal, and use this code-> 
  'ls' -> lists your files and folders
  'cd "folder of your local repo" -> if your desired folder is in         another folder, you can just continue to 'cd' into folders until you    find your right folder. 
  
  check to see if you are in the right folder by typing 'pwd' or "print working directory". 

  Once you've confirmed that you are in the right folder, copy the HTTPS link from your github repo (refer to image below) 
  
  <img width="926" height="694" alt="image" src="https://github.com/user-attachments/assets/d535a3a6-324e-4503-a6d9-bbf2ee73dfe5" />)

 <pre> 
   <code class="hljs langauage-shell"> 
   (base) ucr-secure-01-fs-10-12-135-176:test froglord$ git clone https://github.com/leann-labra/test.git
   Cloning into 'test'...
   remote: Enumerating objects: 3, done.
   remote: Counting objects: 100% (3/3), done.
   remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
   Receiving objects: 100% (3/3), done.</code>
 </pre>







  








