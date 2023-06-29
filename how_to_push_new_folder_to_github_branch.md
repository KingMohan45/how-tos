## Few steps to push a new folder to a github branch

---

1. The folder you wanted to push, run `git init` to initialize the folder as a git repository
2. `git add .` to add all the files in the folder to the staging area
3. `git commit -m "your commit message"` to commit the changes
4. `git remote add origin <your github repo url>` this will create kind of link between remote github repo to local folder. Example - `git remote add origin https://github.com/KingMohan45/node-express-jest.git`
5. Confirm the remote origin is added by running `git remote -v`
   > Pushing the code
6. `git push origin main` to push the changes to the main branch, if you want to push to a different branch, replace `main` with the branch name
7. If you want to push to a new branch, run `git checkout -b <new branch name>` to create a new branch and switch to it
8. Run `git push origin <new branch name>` to push the changes to the new branch
9. If you want to push to an existing branch, run `git checkout <existing branch name>` to switch to the existing branch
10. Run `git push origin <existing branch name>` to push the changes to the existing branch
11. If you get an error saying `fatal: The current branch <branch name> has no upstream branch.` run `git push --set-upstream origin <branch name>` to set the upstream branch
    > Merge conflicts
12. If you get an error saying `fatal: refusing to merge unrelated histories` run `git pull origin <branch name> --allow-unrelated-histories` to pull the changes from the remote branch and then resolve conflicts if any

- basicallly, you are pulling the changes from the remote branch to your local branch and then pushing the changes to the remote branch again to resolve the conflicts, conflict is when you and your team member are working on the same file and you both have made changes to the same line of code, git will not know which change to keep and which one to discard, so it will ask you to resolve the conflict
