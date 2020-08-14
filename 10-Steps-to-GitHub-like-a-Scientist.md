---
output: pdf_document
---
Nowadays, scientists need to be transparent with their code so others can reproduce their work. GitHub is a really handy way to keep track of your code and share it with others because it's super good at version control. 

Indeed, the version control aspect of GitHub has major implications for how you can keep your project folder clean. No more outdated spreadsheets! Save over them... and if you need them, you can just find them on GitHub's timeline, which saves every "commit" (aka update) you've made. 

_Just FYI, the guy who invented Linux OS also created [Git](https://www.sbf5.com/~cduan/technical/git/), the most popular software for developers to co-develop and track changes in their code. GitHub is one of many (but probably the top) websites that can host your work in Git._

If you're already cool with basic GitHub, skip to Step 5. 

## Step 1: Get a GitHub account!
Super easy, just go to [GitHub](https://github.com/) and register your username.

## Step 2: Download the GUI client
The Graphical User Interface (GUI) helps you manage files through your computer. This is very handy when you're managing files you can edit offline as well as those you and others can edit online via GitHub.

[Download here](https://desktop.github.com/)

## Step 3: Make your first repo
Repos are the life-blood of your GitHub. Making a repo allows you to start a shareable project. You should have 1 repo per project (i.e. publishable paper) so all your code is there when you publish (yep, you can link to your GitHub repo in your paper).

### Make one from scratch on the GitHub website: 
1. Click Repositories and hit the big green "New" button. 
2. Make a nice name and description
3. Public vs Private: the Weisbecker Lab policy is to choose a Public repo unless there's a really good reason to keep it secret (chances of getting scooped off of GitHub are vanishingly small).
4. Definitely initialize with a README file. Sharing your code means you need to make it user-friendly, too!
5. Don't worry about the last two options, we'll come back to the .gitignore file in Step 10. 

Now, you can drag and drop code, data, and other related files into the new repo to publish it. This might be a nice option for simple coding projects you finished a while ago. (If not, you can always [delete the repo later](https://stackoverflow.com/questions/11302639/delete-forked-repo-from-github)).

## Step 4: Fork your first repo
Forking a repo from someone else allows you to copy their code and make your own alterations to it (without changing their original). Try forking a repo from someone in the Weisbecker lab by: 
1. Choosing [a repo from this list](https://github.com/orlinst/Vera-s-Lab/blob/master/README.md)
2. Hit the green "Clone or download" button on the right
3. Choose "Open in Desktop", which should launch your GitHub GUI
4. Save to a folder that makes sense on your computer

Now it's yours to tinker!

If you want to add it to your GitHub page (maybe after you've made improvements or alterations), see if you can apply the steps explained in Step 6.

## Step 5: Git your current project's folder ready
What we really want to do is make a repo that comes from a folder - which includes data and code - for a project you're actively working on. 

First, we need to whip that folder into shape. No messy folders on GitHub, that's just embarrassing. From here on, we're going to use a folder system recommended by a lot of coder/scientists, including our very own Dr. Thomas Guillerme! Read his short presentation on [organizing files for reproducible code here](https://github.com/TGuillermeTeaching/OrganiseProjects/blob/master/Presentation/OrganiseProjects.pdf).

Basically, we want the following folders and file at the top level:
* Data/  _(ONLY data!)_
* Functions/  _(NO data!)_
* Analysis/   _(only science - like figures, tables, etc)_
* Manuscript/  _(only writing and publisher-ready figures & table)_
* README.md _(this is the all important overview file - don't worry you can make it in GitHub or skip to Step 10 for a shortcut to making all of the above)_

Take 20 minutes to reorganize/recycle your files so they go into the folders above/the bin. You can up your game further by following [Thomas's instructions](https://github.com/TGuillermeTeaching/OrganiseProjects/blob/master/Presentation/OrganiseProjects.pdf) for folders within those folders. 

## Step 6: Git your project folder into GitHub
1. Go to your GUI client 
2. Press the "+" button on the top left corner
3. At the top of the new dialogue window, click "Add" to the left of "Create"
4. Browse for that project folder you just cleaned up
5. Hit "Create & Add Repository"

You'll see your GUI fill with all the folders and files from your project. Some of these you might not recognize, like .Rhistory because they are hidden from the Finder view. For now, just uncheck the files you don't want to add. We'll go over a faster way to deal with them in Step 10. 

Hit "Commit to Master" then refresh your GitHub page to see the new repo arrive! Note how you've made a new point on your repo's timeline. This is how you can travel back to earlier versions.

## Step 7: Make changes to your code online
Now that your code is in GitHub, you might like to see how it looks to others. 

If someone wants to use your code to start their project, this is what they would fork to edit. (If you work with a collaborator, you can edit the code together with the branch and pull request system explained [here](https://guides.github.com/activities/hello-world/)).

You can make changes to files online by clicking on their filenames and then hitting the pencil button to edit.

## Step 8: Sync those changes with your computer
Imagine you or your collaborator made edits online, you need to sync those before making more changes. Even if you're not collaborating on this project, it's still a good habit hit sync first.
1. Go to your GUI client
2. Select the repo you want to sync on the left hand side
3. Click the sync button on the top right or hit command-S

## Step 9: Make offline changes and commit them to GitHub
Now that you have the most up-to-date version of the repo on your computer, you can make changes the way you normally would. 

For example, edit some code in RStudio or update a data file in Excel.

### Here's how to update your repo with these improvements:
1. Open the GUI client, the files you have changed will pop up there
2. Underneath are some text boxes to explain what you changed. Give a short title and then write a description of the big changes. This will help you massively if you need to go back to an old version of your code before a certain change. 
3. Hit Commit to master!
4. This should update your code in GitHub. If not, refresh the page. If it's still not there, go back to your GUI client and hit sync. 

Hooray! You are now working in GitHub. All your changes are automatically saved, so you don't have to keep a confusing number of files (only a portion of which worked/were the most recent). 

## Step 10: Make a new GitHub-worthy project folder super fast
Ready for a new project? Awesome. You can set up a new project folder with the recommended folder structure in no time using Thomas's [shell script here](https://github.com/TGuillerme/Coding/blob/master/Misc/make.project.sh).

### Take a look at the script by following the link above. You'll notice it does 3 main things:
1. It will ask you for a PROJECT-NAME. This should be a short, descriptive title - it will become the title for the project repo and a number of important files within those folders, too.
2. Next, it makes all those folders! Note especially, the 3 different folder types under Data/. Return to [Thomas's guide for organizing folders](https://github.com/TGuillermeTeaching/OrganiseProjects/blob/master/Presentation/OrganiseProjects.pdf) for best practices. 
3. Finally, it makes some general files which all coding project should have. The README.md file and the .gitignore file.

Let's take a minute to really look at that .gitignore file. It's purpose is actually pretty self-explanatory, it tells Git (and in our case, GitHub) which files to automatically ignore or pass over when uploading changes and new files to the repo. Remember all those files we didn't recognize when we first committed a folder to GitHub in Step 6? They will automatically be ignored now that their file names or extensions are in the .gitignore file. This also reduces the size of our repos, which keeps them running smoothly. 

### Running the shell script takes a little foray into the terminal. 
1. Download [the shell file](https://github.com/TGuillerme/Coding/blob/master/Misc/make.project.sh) from Thomas's GitHub by clicking on the computer icon "Open this file in GitHub Desktop." This should take you to the folder in your Finder where it is now stored. Keep that Finder window open.
2. Open Terminal.
3. First change the directory to the folder that has the .sh file by typing cd (space) and dragging the folder from the finder window into the terminal line so it looks like this:
> cd /path/to/directory
4. Now, tell the Terminal to run that sh file and (space) give it the project name like so:
> sh make.project.sh awesome-project-name

Boom! Your new folder will pop up in the same folder as the .sh file. Drag it into the folder where you keep your projects and you're off. 

### Congrats! You are GitHub ready! To learn more about making your code more efficient and human-readable, check out the [Tips for Writing Good Code page](https://github.com/orlinst/Vera-s-Lab/wiki/Tips-for-Writing-Good-Code). 

## Bonus Step: Make a personal GitHub page
This is a site hosted on GitHub where you can upload your CV or anything else you want by following [these instructions](https://pages.github.com/). Under Q1, choose Desktop Client as your Git Client (unless you prefer the terminal of course). 

Thomas has more advice [here](https://github.com/TGuillerme/Teaching/blob/master/GitHubPages_Demo/GitHubPages.pdf).

Once it's set up, you can feature it on your GitHub account. Click your little Account picture on the top right > Settings > paste in the github.io URL into the URL box.