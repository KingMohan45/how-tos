## Few steps to push a new folder to a github branch

---

1. To add all the files in the folder to the staging area, use the following command:
```
git add .
```


2. To commit the changes use
```
git commit -m "your commit message"
```


3. To create a link between the remote GitHub repository and the local folder, run:
```
git remote add origin <your github repo url>
```
For example:
```
git remote add origin https://github.com/KingMohan45/node-express-jest.git
```

4. Confirm that the remote origin is added by running 
```
git remote -v
````

## Pushing the code

- To push the changes to the main branch, use the command:
```
git push origin main
```
If you want to push to a different branch, replace `main` with the branch name.

- If you encounter an error saying `fatal: The current branch <branch name> has no upstream branch.`, to set the upstream branch run 
```
git push --set-upstream origin <branch name>
```

## Merge conflicts

- If you receive an error saying `fatal: refusing to merge unrelated histories`, to merge the unrelated histories of the branches. Resolve any conflicts that arise and then push the changes to the remote branchm run 
```
git merge origin/<branch name>  --allow-unrelated-histories
``` 

- basicallly, you are pulling the changes from the remote branch to your local branch and then pushing the changes to the remote branch again to resolve the conflicts, conflict is when you and your team member are working on the same file and you both have made changes to the same line of code, git will not know which change to keep and which one to discard, so it will ask you to resolve the conflict
