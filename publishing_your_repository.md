# Publishing your repository

Before you can push your local repository to GitHub you first need to create an empty repository.

A repository is a storage space where you can access your project, its files, and all the versions of its files that Git saves.

When you browse to your GitHub account you can click on the new repository button. The button looks like a plus sign and is found at the top right of the website. Alternatively, you can simply browse to https://github.com/new (Links to an external site.)

Fill in the name your repository and
click the large green button at the bottom of the page to finish the process of creating it.
Your repository will be located at https://github.com/<your GitHub user name>/MyNewRepository
  Now that you have a repository you can go back to your PC and push your existing repository to the one you just created.

Make sure you have completed the activity to configure your commit author and email. 

Next, you need to tell your local version of Git about the remote repository. Your local branch is called master. Your remote branch is called origin.

You do this by typing git remote add origin https://github.com/<your GitHub user name>/Products

The git remote command is used to add a new remote section called origin to our configuration.  To check if you have the remote repository initialized you can view the git configuration with git config --list as described here.

Running git remote without any arguments will show you the remote repository aliases.

If you run the command with the -v option, as git remote -v, you can see the actual URL for each alias.

If you want to share a locally created repository, or you want to take contributions from someone else's repository it's generally easiest to add it as a remote.