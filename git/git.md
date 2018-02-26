todo
=====
* workflows


overview
==========
4 areas: stash, working, index (staging), repo
messages: present tense (recommended style)
objects (commits, ??): immutable

golden rule
=============
never change shared history (eg: rebase shared commits).

amend commit
==============
can change message, etc
git actually copies current commit to new commit with amendments; 
  * like a small rebase
  * old commit will be gc eventually

git commit --amend
* amend latest commit

fix earlier commit
===================
for last commit, use --amend. otherwise, ...
keep golden rule in mind. 

make brand-new commit, then squash new + old commit into single object.



unstage file
=============
todo




git log examples
====================
git log --graph --decorate --oneline
git log <branch1>..<branch2> --oneline : show all new commits


--patch
--grep



rebase interactive
===================
git rebase -i origin/master
git rebase --continue

* super-powerful history editing tool (reorder, squash, etc)
* evolved to mean "change history"
* from given commit (excluded) onwards
* list of commits is from least recent -> most recents (opposite that of git log)
* mini-program whose output is the new history

* reword commit msg
* squash commit



