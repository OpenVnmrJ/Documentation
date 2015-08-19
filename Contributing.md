#Contributing#
##Our Philosophy##

###Low barrier of entry###

We strive for a low barrier of entry to the project. This is partly achieved by not requiring new contributors to “prove themselves” before they are admitted to the committership.[?] Instead, we assume they are good until proven otherwise, and this principle applies to anybody without 
arbitrary discrimination. We recognize that every contribution is precious, and we recognize that every added process turn away some potential contributors.

The lower barrier of entry is partly achieved by structuring the project to core, pulse programs, macros, documentation, and other independent pieces, thereby reducing the need for extended collaboration and communication. We try to let everyone have their own turf where they can work efficiently without bogged down by discussions and compromises. 

The lower barrier of entry is also partly achieved by recognizing that people move on. Lots of code in the project is maintained by people other than the original author. We encourage new contributors to take over existing projects that aren’t actively maintained. We believe that “old” contributors deserve respect from “new” contributors, but the inaction on the part of the original contributors shall not block new contributors from making changes.

Even users unfamiliar with code can contribute: file bugs on github, let the developers know what is important to you, suggest improvements, and join discussions

###Meritocracy###

Our striving to a low barrier of entry doesn’t mean everyone has the equal voice. We value those who contribute more to the project, namely Meritocracy. Contribution shouldn’t be narrowly interpreted just as code changes, but rather it includes such activities as helping others in the OpenVnmrJ community, producing documentation, running infrastructure, and so on.

###Transparency###

We believe in running the project transparently. This includes everything from decision-making to defects in the code.

###Compatibility matters###

We recognize that users expect their existing data, accumulated under past versions (including commercial versions) to continue working under future versions of OpenVnmrJ. This includes jobs configurations, build records, and spectrometer configurations that they are using. The OpenVnmrJ project places high value on maintaining this compatibility, and will be very careful in removing functionality.

The use of modules, called applications directories, is strongly encouraged for adding functionality that is large in scope.


###Technical details###

The github repository is https://github.com/OpenVnmrJ/ and only a documentation page exists at this time. Sign up for a free github account to access the repository. With github all changes are made offline and merged back in.

You’ll need to have git (a set of command line programs) installed on your computer and a git UI if you are uncomfortable with the command line, see:
https://windows.github.com 
https://mac.github.com
http://gitx.frim.nl

On Ubuntu: sudo apt-get install gitk

###Git workflow###
_This is for a public repository. Initially, the repository is private until copyright is transfered to wither Orgeon or Stanford_

A "quick" summary of how to use change/add files is:

1. Fork the repository into your own account (Use github UI, see https://help.github.com/articles/fork-a-repo/)
2. Download the repository to your computer (Use github UI or git clone https://github.com/YOURREPO/Documentation.git)
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
