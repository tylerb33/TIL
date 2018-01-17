### GitHub removing directory

I had an issue where there was a directory existing on GitHub but not in my local directory. I believe caused by a misspelling somwhere along the way (Javascript vs. JavaScript). 

1. I made a new branch then used the command ```git rm -r --cached Javascript```, then I committed.

1. I was able to push this branch up to GH.

1. However, when trying to switch back to master I had to run the following commands (contents of the folder I removed):

```rm Javascript/closures.md```
```rm Javascript/general-js.md```

NOTE: this could potentially delete those files all together. Since they were still open in Sublime, I was able to simply re-save them in the new, correct, ```JavaScript``` directory so I didn't lose them.

1. Once those were removed, I was able to checkout to master and pull origin from GH.