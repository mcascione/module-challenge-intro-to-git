## Research Questions 

Now that you are all set up, it's time to learn a little more about the tools of the trade. Edit this file and answer the following questions. You are going to need to start familiarizing yourself with the [GitHub docs](https://docs.github.com/en). Docs (short for documentation) are the instructions on how to use a languge or program. A large part of your job as a developer will be learning how to read and work with documentation. Please reference the GitHub docs when answering the questions below. If you cannot find what you are looking for in the docs, you can always start to practice your Google skills!

1. What is Git? 
Git is an open source version control system (VCS) that allows you to keep track of changes made to local files on your computer. Version control allows 
2. What is the difference between Git and GitHub?
Git is an underlying system of commands that you run in your terminal to manage your code. Changes are saved locally as commits that can be accessed later to review or reload. 

GitHub is a cloud product that holds or stores code in repositories that can be accessed remotely and simultaneously by multiple developers.
3. Why do we create a branch? 
Branching allows for clean and simultaneous collaboration on the same repository. You can create a local copy of the main branch to work on it on your own before merging it back to the main code.
4. What is the purpose of a Pull Request?
A pull request is a summary of changes that you have made to a branch of code. It notifies other developers that you have made changes that need to be reviewed. The pull request makes evident the changes by means of a comparison of your feature or bug fix branch with the main branch. Once your pull request is reviewed by a developer, they can either leave comments or merge your request. The changes that you made will then be deployed into the main branch.
5. What is the command you can use to switch between branches? For example you are working on FIRSTNAME-LASTNAME branch and you want to switch back to main.
`git checkout <branch-name>` or `git switch <branch-name>`
6. Explain the difference between `git fetch`, `git merge` and `git pull`. What does each command do?
The `git pull` command fetches and downloads changes from a remote repository and then merges those changes into a local repository. The `git pull` command combines `git fetch` and `git merge` into just one command. To review the changes before committing them, you can first use `git fetch` to add changes to your local repository and review the changes followed by `get merge` to merge the changes.

`git pull` fetches changes and merges them. You can use `git pull` to merge changes that were made to a remote file and pull them in to your local copy to make sure it is up to date. 

`git fetch` takes changes from the remote repository and adds them to your local working branch but does not commit them. You can review the changes before committing them to your local branch.

`git merge` takes the changes from one branch and applies them to another branch. This is done within the same repository or from a fork. 
7. What is a merge conflict?
If a change is made to code that conflicts with another change, it produces a merge conflict that pauses the merging process and must be resolved. 

This typically happens when two developers have made changes to the same line of code, or if a file was deleted by one developer while being modified by another developer. 

Git does not know which change is correct so the developer that is conducting a merge will see a merge conflict. Git will mark the file being merged as conflicted and pause the merging process. The developer must then resolved the conflict. 
8. How do you resolve a merge conflict?
There are different types of merge conflicts that require different resolutions. 

Competing line change merge conflicts can be resolved by selecting the correct change to incorporate from the different branches. You will need to merge the new commit before you can merge the branches.

To do this, navigate into the local Git repository that has the merge conflict using cd REPOSITORY-NAME. Then you can use `git status` to generate a list of the files affected by the merge conflict. Open these files in your code editor and search for the conflict marker <<<<. Your changes will be listed under =======. Select which changes you want to keep, make your changes and delete the conflict markers. Add and commit your saved changes using `git add .` and `git commit -m "<insert message about your choices here>"` Finally, merge the branches by pushing your changes to your remote repository and completing a pull request.

A similar process is used to resolve competing file change merge conflicts. However, in this case, you will decide whether to delete or keep the file with a new commit. 

Skipping to the step where you have opened the removed file in your code editor, you can either add the removed file back to your repository using `git add <filename>` or remove it using `git rm <filename>`. You would then commit your changes using `git commit -m "<insert message about resolving merge conflict explaining whether you kept it or deleted the file>"` and then merge your branches with `git push` and a subsequent pull request. 