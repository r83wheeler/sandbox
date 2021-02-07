# sandbox

# create new project
    1. creat the project folder in /Sites
    2. cd into the project folder
    3. mkdir gitExample
    4. git init - initialize an empty git repo

# create or update a file
    1. creat a file with touch or echo
    2. git status - shows info (branch, if there are commits, tracked and untracked files)
    2. git add . or -A or (the file name)
    3. git commit -m "specific thing that was done"

# adding a Remote repo 
    1. git remote add (alias name of remote repo (origin)) (the gitHub URL) -https://github.com/r83wheeler/splash.git

# add changes to remote
    1. git push (name of remote (_ususally origin)) name of a branch (main or dev or a working branch(name whatever you want))


# pull changes from remote
    1. git chechout main 
    2. git pull origin main
    3. update dev and working branches by doing the following 
        a. git chechout dev 
        b. git merge main
        c. (optional) repeat a. and b. for each working branch that needs updating 
    4. git push origin dev or (working branch)

# create a pull request
    1. navigate to the remote repo on github
    2. create a pull request from dev or working branch into the target branch
    3. confirm the pull request if it has not conflicts
        a. if conflicts, they need to be fixed locally first and pushed up in order to resolve the conflicts
    4. complete the pull request 
    5. pull changes from remote 

# clone remote repo
    1. navigate to the remote repo on github
    2. copy the github URL of the remote repo
    3. in terminal, navigate to /sites
    4. git clone (github URL)
    5. cd into new folder created by gitclone
