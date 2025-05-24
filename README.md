## test creation of a new project
now I pushed this README.me to Github.
I created a new fine grained personal token to succesfully login. I had to set individual permissions.

## Commands

git remote add origin https://github.com/zididadaday/test-project

This will add a location to store your files named origin.

github commit -a

This will save all your changes.

git push -u origin main

Will push your changes to your git repository called origin.


## More tips

I got tired of having to enter my credentials and key on every commit.

git config --global credential.helper store
git config --global credential.useHttpPath true

Will update your ~/.gitconfig and tell git to store your credentials in a ~/.gitcredentials file for the given repository.
