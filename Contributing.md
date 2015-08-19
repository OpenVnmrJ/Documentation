The github repository is https://github.com/OpenVnmrJ/ and only a documentation page exists at this time. Sign up for a free github account to access the repository. With github all changes are made offline and merged back in.

You’ll need to have git (a set of command line programs) installed on your computer and a git UI if you are uncomfortable with the command line, see:
https://windows.github.com 
https://mac.github.com
http://gitx.frim.nl

On Ubuntu: sudo apt-get install gitk

A "quick" summary of how to use change/add files is:

1. Fork the repository into your own account (Use github UI, see https://help.github.com/articles/fork-a-repo/)
2. Download the repository to your computer (Use github UI or git clone https://github.com/[YOURREPO]/Documentation.git)
3. Checkout the development branch: git checkout development (I need to make a development branch!)
4. Start your branch git checkout -b "my feature" (see branches below) Always start a new branch for your work, so it can be merged in later, and branch from development, not master
5. Make your changes, add, delete files on your own computer
6. Commit your changes
7a. Rebase from the development branch (to merge in any new changes to the documentation)
7b. Rebase interactive to squash your commits (good if you’ve got many commits)
8. Push your changes back to your fork
9. Make a pull request back to the development branch, see Git Pulls

 A bit complicated for one page, but it works well with hundreds of files and hundreds of contributors.


Branches
git checkout -b "my feature"
See https://www.atlassian.com/git/tutorials/using-branches/git-checkout how to make a branch ind use branches
See http://nvie.com/posts/a-successful-git-branching-model/ for how this applies to a real project

Git pulls
See https://help.github.com/articles/using-pull-requests/
“Fork and pull” model is good for this project (when there are more contributors).
The GitHub UI can be used. Review the changes and 
git merge --no-ff <branch>
