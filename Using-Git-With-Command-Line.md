# Using Git With Command Line

Command line is one of the most powerful tools you will ever use, but it becomes powerful only after you learn it, breathe it, and embrace it. Today we'll take a brief look at Git and using Github with the command line on Linux or Mac OS.

Let's take this step by step

## Step 0: Install git and create a GitHub account 

The first two things you'll want to do are install git and create a free GitHub account. Accounts are free for public repositories, but there's a charge for private repositories.

With your favorite package manager install git on your local machine. It should be as easy as `apt-get install git` or `yum install git`.

This is step 0 as it is required for virtually anything we do with Github or git.

## Step 1: Create a local git repository 

Open the terminal and create a new folder somewhere you prefer, maybe on Desktop or maybe in ~/Documents/School/Projects/Github. Depends entirely on you.

Once you have the folder, `cd` inside it and run `git init` command. It should return "Initialized empty Git repository in <your directory>"

## Step 2: Add a new file to the repo

Your repository looks rather empty at the moment, let's add a file to it and make sure it's properly populated. To do this you're going to either create in or move the file to the directory you chose, I trust you know how to do this.

Once you have the file run the command `git status` to quickly see which files git is currently aware of. At this particular point it should have no files and should tell you about the untracked files you have in the directory. Run `git add <name of the file>` or `git add .` (the period at the end adds all files in the directory)

## Step 3: Commit the file

Git now tracks the file locally, but you still need to commit it to the repository online. Let's do that with `git commit`. Additionally, you can get around adding comments in a new window but adding an "m" flag, just like this: `git commit -m "This is my first commit!"`. Now you should see something like "1 file changed, 1 insertion(+)"

Very important:
Don't put a message like "asdfadsf" or "foobar". That makes the other people who see your commit sad. Very, very, sad.

# Some additional useful stuff

## Create a new branch

Branches are important in long, complex projects or work performed by mulitple colaborators. It lets you track all the work and only push to master the solutions that have been successfully tested.

It's as easy as `git branch` which should return the new view of your repository and show you the master branch and the new branch

## Push a branch to GitHub

Now we'll push the commit in your branch to your new GitHub repo. This allows other people to see the changes you've made. If they're approved by the repository's owner, the changes can then be merged into the master branch.

We'll have to run a bit longer command here: `git push origin my-new-branch`. What's the "origin"? Well, when you clone a remote repository to your local machine, git creates an alias for you. In nearly all cases this alias is called "origin".

This command should show you how many objects were pushed, and what was the speed of it.

## Get changes on GitHub back to your computer

Right now, the repo on GitHub looks a little different than what you have on your local machine. For example, the commit you made in your branch and merged into the master branch doesn't exist in the master branch on your local machine. We can quickly fix it by running `git pull origin master` which will download all new changes to your local machine

Now we can use the `git log` command again to see all new commits. If you want to check the master directly, you should use `git checkout master` instead.

## That's it

You're done. This is the basics on Git and the Command Line. Stay tuned for the next blog.
