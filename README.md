# Setting up GitHub and Local repos for Pair Programming:

## Person 1 - The Repo Maker:

1. Make new remote repository on GitHub
    - It should be public
    - Name something like WXDX

2. On your computer `cd` to where you wish to store your classwork for the day 
and make a new folder
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
1. Accept the Collaborator invitation via email

2. Retrieve the clone link from your partner's GitHub
    - Click the green `<> Code` button
    - Copy the HTTPS url 

3. On your computer `cd` to where you wish to store your classwork for the day
    - Do NOT make a new folder for `WXDX` 
        - It will be made automatically when you clone your partner's repo
    - Run `git clone <copied clone link>`
    - You now have cloned your partner's repo and have push/pull access

### Optional: Add a copy of your shared work to your own GitHub
1. Make new remote repository on GitHub
    - It should be public
    - The name should match the repo you have cloned
2. In the repo you cloned add a new remote to your freshly made GitHub repo
    - run `git remote add my_github <url to your GitHub repo>.git`
3. Push up all code from your local machine to your GitHub repo
    - run `git push my_github main`
4. You can now push changes to your partner's GitHub repo and your own.
    - To push to your partner's GitHub Repo run `git push` or 
    `git push origin main`
    - To push to your own GitHub repo run `git push my_github main`
    - NOTE: You only need to push to your own GitHub repo at the end of the day.

## Next Steps

- From here on out it is just pushing and pulling as each partner switches off.
    - To pull the most recent changes pushed by your partner run `git pull`
        - This will pull from origin main, the original GitHub repo created by
        Person 1
    - To push the most recent changes you have made run `git push` or 
    `git push origin main`
        - This will push to origin main, the original GitHub repo created by
        Person 1
