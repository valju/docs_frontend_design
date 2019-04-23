Suggested way for people to transition from individual learning code in own branches (or no branches) to integrating the code to the master:     (here 'mike' is an example name for a branch)

1. Take your current edited files to safety, e.g. Desktop\stash\20181030 folder

2. Remove the possibly old and incompatible Backend or Frontend repo folder totally

3. *Clone* it from GitHub.com (While in your case do it in root folder called e.g. Case2019K, not in the repo root folder ). Cloning needed if you are not working with a branch that follows the very same folder and file naming and structures as the master. If not sure, then remove and clone.

4. /// Run both backend and frontend, test them, if needed, run npm install) = make the given ones work together before adding your work. ///

5. Only when you really know what additions/fixes you will do, do a up-to-date *git pull* and then Create your own branch with: *git checkout -b mike* or so, (other possibility would be per feature name, like idea_list_all, idea_add, but for us your name might be best. Or e.g. mike_idea_add telling whose branch, and about what feature )

6. Manually add changed files or codelines from you stash via file explorer

7. *git add -A*     
(To add new files / file deletions / file edits to STAGING AREA of local repo, current branch)

8. *git status*    to see if anything funny seems to be happening (e.g. a lot of added new files when should be none) or all seems legit

9. *git commit -m "Commit description here. Changes and fixes mentioned."*
(To commit the changes to the local repo, current branch. Guidelines say
commit comments should be in present tense, not in past tense: 'Fix db settings', not 'db settings fixed')

10. *git push -u origin mike*           (To share your work to others to see on GitHub, not yet to master branch. If/As you cloned from remote, remote should be configured fine)

11.  (keep on working, fetch and merge from master (git pull) if afraid for master to change too much from your starting point while you work on your own)

12. When ready with features, test well, go to Github.com, *make a pull request* (Ask somebody to carefully review your branch changes to master, and ask them to be pulled and merged to master). So your own branch you can push to remote repo to your own branch, but to master you ask somebody else to pull.

13. When your pull request gets accepted, your branch has no changes to offer to master. Then you can either *delete your branch* or immediately *continue working* with it. And after changes start from step 6 again. (edited) 

Deleting a pulled and merged branch is good signal for others, so they don't assume you are working on it still. We are a lot of people. So nobody will develop in a vacuum, there will be clashing edits, needs for unification, needs for refactoring all the way until the end of the project. Thus it's good to have some kind of idea who might be working on same files as you are. (edited) 

Note: When you have now started to use common backend and common frontend as starting point every day, you don't need to clone anymore. Just start the day by *git pull* in both back&front repo root folders + *git checkout -b mike*    on the one you work with, and so on.

Note: running *git status* is not enough for knowing if the local repo branch is up-to-date with the remote repo version. This command will tell you something like ‘all up-to-date’ even if not true. Thus you actually do have to run *git pull* to really know if there are any updates available in the remote repo.

Git documentation, e.g.
https://mirrors.edge.kernel.org/pub/software/scm/git/docs/gitglossary.html
https://git-scm.com/docs 
https://git-scm.com/book/en/v2

https://www.git-tower.com/blog/git-cheat-sheet  (Cheat sheet of most common commands,
some explanations a bit misleading though)

GitHub.com documentation: 
https://help.github.com/en/articles/github-glossary
https://services.github.com/  
(We are using GitHub.com as remote repo hosting cloud, but could use many other hosting services GitLab, BitBucket, MS TFS, ..., or even set up own remote server repo)
