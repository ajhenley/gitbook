###Book Developer Information

##This information should not be published. Contains helpful information for book editors/developers.


Gitbook is based on mediawiki and git (as you know) proving the adage that there are no new ideas - just new combinations of old ideas.
Here's the git details for gitbook: https://help.gitbook.com/build/push.html

Using git I cloned the book:
```
#git clone https://dave45678@git.gitbook.com/javateach/javaee.git

```
now I can create media wiki formatted files and save them and the images locally in the git folder 

When I'm done editing I can push them back:
```
#git pull
#git add --all
#git commit -m "modified some file"
#git push origin master
```

As an added bonus if you install grep.exe on your computer (just put it in the path) then you can see what needs to be done:
```
#grep todo *.md
```

And there's more! You could write a python script to parse out the java code between the {ace} ... {endace} tags or otherwise search the book for inconsistencies or other issues.


As expected, there's also a python solution: https://www.mediawiki.org/wiki/Manual:Pywikibot/Create_your_own_script


