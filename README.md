# Setting up GitHub and Local repos for Pair Programming:

## Person 1 - The Repo Maker:

1. Make new remote repository on GitHub
    - It should be public
    - Name something like WXDX

2. On your computer cd to where you’ll store your classwork for the day and make 
a new folder:
    - `mkdir WXDX` - keep naming convention the same as you did for GitHub
        - Note: Should NOT be in another git repo
            - double check by running `git status` at in the folder that your new `WXDX` is in
            - should error as fatal: `not a git repository (or any of the parent directories): .git`

3. cd into W3D2 and follow the commands listed on GitHub:
echo "# git-steps" >> README.md
    - `git init`
    - `git add README.md`
    - `git commit -m "first commit"`
    - `git branch -M main`
    - `git remote add origin https://github.com/<github-username>/<github-repo-name>.git`
    - `git push -u origin main`

4. Download skeleton for the day’s project and move into `W3D2`
    - If there isn’t a skeleton, you’ll want to make a new subfolder instead 
    especially if the day has more than one project

5. Add / Commit / Push
    - `git add .` or `git add -A` (be sure to understand the difference)
    - `git commit -m "commit message here"`
    - `git push` defaults to `git push origin main`

7. Add your pair as a collaborator to the repo
    1. On repo page on GitHub, go to settings
    2. Go to Manage Access
    3. Invite collaborator using your pair’s GitHub username

## Person 2 - The cloner:
1. Make new remote repository on GitHub
    - it should be public
    - name should match the repo you will be cloning
2. Navigate to a local folder where you’ll ‘store your classwork’
    - Do NOT make a new subfolder for wXdY - that will be made when cloning
    - Double check that you are not within an existing git repo by running git status
3. Clone your pair’s repo
    - (Either following the link from your pair or they can directly send you the url you’ll need to clone)
4. Within the newly cloned repo, run git remote - you’ll see the source of the clone is automatically added as a remote named origin
5. Add a new remote with YOUR remote GitHub repository
    - Still just git remote add <name for remote> <remote url>
    - Name the remote your name (for example git remote add daniel https://github.com/danielsgithub/w40d3 )
6. Run git remote to verify/show you now have two remotes
7. Push to your GitHub repository to verify that your remote is set up properly
    - you HAVE to specify where you’re pushing, as just git push will push to origin
    - ex: git push peter main
8. Make a change to the files (representing your turn driving), add, commit
9. Push the change to origin by just running git push or by running git push origin main
    - you CAN push to both, but no need to do that every time you switch
10. Change will have been made to your pair’s remote repo, but not to yours!

Person 1:
1. Pull changes from origin
2. Will be exactly where your pair left off
3. Make changes to the code
4. Add/commit/push to origin

Person 2:
1. Pull changes from origin
2. Make changes (representing the last work of the day) and add/commit
3. Push to origin and then also push to YOUR remote repo - BOTH will have the final state of the project
4. Add link to repo to PT for the day, where it asks for your classwork repo (edited)