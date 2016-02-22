###Working with Others

When working on a team one person will create a very basic project and a repository. Next they should check the basic project into the new repository on GitHub.

Using git on your local computer, you can clone the other project to get a local copy:
```
#git clone https://github.com/gitusername/gitrepositoryname
```
Now you can modify the files locally and even add or remove files. 
You should coordinate with your team mates so two people are not simultaneously working on the same file. When this happens you have to merge the two files and decide which changes to keep or discard.

When you are done editing you can push your changes back to the team's repository. Allways run ```git pull``` before adding files. That way you will get the latest version and minimize conflicts.

####The following commands will synchronize your local and remote repository
```
#git pull
#git add .
#git commit -m "modified some file"
#git push origin master
```


