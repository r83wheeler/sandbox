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

# fatal: refusing to merge unrelated histories
    1. occurs when two unrelated projects are merged 
    2. You have cloned a project and, somehow, the .git directory got deleted or corrupted. This leads Git to be unaware of your local history and will, therefore, cause it to throw this error when you try to push to or pull from the remote repository.
    3. You have created a new repository, added a few commits to it, and now you are trying to pull from a remote repository that already has some commits of its own. Git will also throw the error in this case, since it has no idea how the two projects are related.
    4. Solution
The error is resolved by toggling the allow-unrelated-histories switch. After a git pull or git merge command, add the following tag:

git pull origin master --allow-unrelated-histories

# fatal: origin does not appear to be a Git repository
    1. By default, a Git repository is not associated with a remote repository. If you try to push changes to a remote repository without first specifying its location, you’ll encounter the “fatal: ‘origin’ does not appear to be a git repository” error.
    2. The git init command creates a new Git repository. This command only initializes a folder as a Git repository. It does not link a repository to a remote repository.
    3. The “fatal: ‘origin’ does not appear to be a git repository” error occurs when you set up a new repository and try to commit code without first instructing Git on where the code should be pushed.
    4. To fix this error, we need to manually tell Git where the remote version of our repository exists. Do this using the git remote add command:

git remote add origin https://github.com/r83wheeler/"repoName".git

This command tells Git the remote called “origin” should be associated with a particular URL. Git now knows where the remote version of our repository exists.

