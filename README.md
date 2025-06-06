## test creation of a new project
now I pushed this README.me to Github.
I created a new fine grained personal token to succesfully login. I had to set individual permissions.

## Commands

`mkdir test-project`

Create a local directory to store your project.

`cd test-project`

Change to the project directory.

`git init`

Initialize your new project.

`touch README.md`

create a README.md file.

`git commit -m "first commit"`

commit your first changes

`git branch -M main`

select the branch of your project

`git remote add origin https://github.com/zididadaday/test-project`

This will add a location to store your files named origin.

`git add -A`

This will add all new files you have added to your project.
Without the `-A` option you can add specific files.

`git commit -a`

This will save all your changes.

`git push -u origin main`

Will push your changes to your git repository called origin, branch main


## More tips

I got tired of having to enter my credentials and key on every commit.
```
git config --global credential.helper store
git config --global credential.useHttpPath true
```
Will update your ~/.gitconfig and tell git to store your credentials in a ~/.gitcredentials file for the given repository.

## Permissions required for the token

What Repository permissions should you add to the token? (principle of least privilege)

- Actions
- Administration
- ~Codespaces~
- Commit statuses
- Contents
- Metadata
- Pull requests

## Generate a git -diff for two folders

```
## --no-index is the way to go, here we are just getting diffstat to give us a summary of changes
git diff --no-index --patch --summary folder1/ folder2/ | diffstat > summary-of-changes.patch
## here we have removed diffstat, generating a patch
git diff --no-index --patch --summary folder1/ folder2/ > changes.patch

## here we put the summary of changes and patch into one file
echo --- > final.patch
cat summary-of-changes.patch changes.patch >> final.patch

## here we apply the patch
patch --dry-run -p1 -ruN -d original2 < final.patch
patch -p1 -ruN -d original2 < final.patch
```

## Useful links

[https://git-scm.com/docs/git-push](https://git-scm.com/docs/git-push)

[https://stackoverflow.com/questions/74493073/using-a-github-fine-grained-token-with-git-pull-over-https](https://stackoverflow.com/questions/74493073/using-a-github-fine-grained-token-with-git-pull-over-https)
