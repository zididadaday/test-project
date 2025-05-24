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

`github commit -a`

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

What permissions should you add to the token? (principle of least privilege)

```
Actions
Administration
Codespaces
Commit statuses
Contents
Metadata
Pull requests
```

## Useful links

[Git documentation on git push](https://git-scm.com/docs/git-push)

[https://stackoverflow.com/questions/74493073/using-a-github-fine-grained-token-with-git-pull-over-https](https://stackoverflow.com/questions/74493073/using-a-github-fine-grained-token-with-git-pull-over-https)
