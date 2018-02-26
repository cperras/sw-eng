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

local workflow
===============
* commit early and often. tests may still be broken, temporary commit messages, etc. (can revert to previous state).
* to checkpoint, perform interactive rebase to make it nice and clean, then push.

revert commit
===================
* works with shared history; updates history safely (caveat: merges)
* old broken commit stays in history
* git revert 
* reverses original commit (creates new commit)
* catch: can't revert structure of change (eg: merge), which can cause some confusion.
* be careful when reverting merging commits!!

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

recover hash of abandoned object
------------------------------------
* eg: accidentally delete commit. to undo,  put a branch on it so it's no longer abandoned.
* git reflog refs/heads/master
* until it is garbage collected.... 


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



