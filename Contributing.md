#Contributing#
##Our Philosophy##

###Low barrier of entry###

We strive for a low barrier of entry to the project. This is partly achieved by not requiring new contributors to “prove themselves” before they are admitted to the "committership" (or soe other honorific).  Instead, we assume that all contributors are good until proven otherwise, and this principle applies to anybody without arbitrary discrimination. We recognize that every contribution is precious, and we recognize that every added process turns away some potential contributors.

The lower barrier of entry is partly achieved by separating the project into "core", "appdirs" (groups of pulse programs, macros, & templates), documentation, and other independent pieces, thereby reducing the need for extended collaboration and communication. We try to let everyone choose their own turf where they can work efficiently without bogged down by too many discussions and compromises.

The lower barrier of entry is also partly achieved by recognizing that people move on. Lots of code in the project is maintained by people other than the original author. We encourage new contributors to take over existing parts that aren’t actively maintained. We believe that “old” contributors deserve respect from “new” contributors, but the inaction on the part of the original contributors shall not block new contributors from making changes.

Even users unfamiliar with code can contribute: install and run the development versions of OVJ, file bugs on github, let the developers know what features/fixes are important to you, suggest improvements, and join discussions

###Meritocracy###

Our striving to a low barrier of entry doesn’t mean everyone has the equal voice. We value those who contribute more to the project, namely Meritocracy. Contribution shouldn’t be narrowly interpreted just as code changes, but rather it includes such activities as helping others in the OpenVnmrJ community, producing documentation, running infrastructure, and so on.

###Transparency###

We believe in running the project transparently. This includes everything from decision-making to defects in the code.

###Compatibility matters###

We recognize that users expect their existing data, accumulated under past versions (including commercial versions) to continue working under future versions of OpenVnmrJ. This includes pulse sequences, macros, and spectrometer configurations that they are using. The OpenVnmrJ project places high value on maintaining this compatibility, and will be very careful in removing functionality.

The use of modules, called applications directories (or "appdirs"), is strongly encouraged (if not mandatory) for adding any functionality that is large in scope. Also in this spirit, minimizing any needed changes to the "core" code for new features is strongly preferred.

##How to join this project##

See the document How to Join.md for more details.

##Technical details##

The github repository is https://github.com/OpenVnmrJ/ and only a documentation page exists at this time. Sign up for a free github account to access the repository. With github all changes are made offline and merged back in.

You’ll need to have git (a set of command line programs) installed on your computer and/or a git UI (if you are uncomfortable with the command line), see:
https://windows.github.com
https://mac.github.com
http://gitx.frim.nl

On Ubuntu: sudo apt-get install gitk

###Branch information###

OVJ code is developed on 2 main branches

*Master: This will produce the final compiled downloadable archives. It must be kept clean of bugs! Unless it is a critical bug-fix, no new code should be branched directly from Master.

*Development: This is the current working branch. To add new code or documentation to OVJ, create a feature branch (name it something descriptive) from the Development branch. When your feature branch is complete, make a pull request back into Development. Once Development is validated and tested, the code can be pushed into Master.

If we have a cycle of regular development, we may have version branches.

###Appdirs###

OVJ uses Appdirs; modular code that resides in "Application Directories" and can be optionally loaded at run-time to reconfigure the UI, pulse sequences, macros, etc. If a new feature can be implemented via a Appdir without changes to the Core OVJ code, this is greatly preferable.

If you have minor features to add or changes to existing macros, templates, or pulse sequences, please put this work in the "develop" Appdir ("/common/develop"). When a new release of OVJ is made, the "develop" Appdir will be merged into a release Appdir.

If you have a significantly new feature or a very large number of files and changes, you should make your own new, separate Appdir (with its own name) in the Development branch of the OVJ code.

###Important tips###

*Always work from a feature branch. Since all code submissions will be through a Pull Request, feature branches isolate changes from one submission to another.
*Always start your new branch from the branch you want to submit to: git checkout -b myfeature development
Remember to submit your Pull Request to the proper dev- branch and not master or 3.x

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


###Branches###
git checkout -b "my feature"
See https://www.atlassian.com/git/tutorials/using-branches/git-checkout how to make a branch ind use branches
See http://nvie.com/posts/a-successful-git-branching-model/ for how this applies to a real project

###Git pulls###
See https://help.github.com/articles/using-pull-requests/
“Fork and pull” model is good for this project (when there are more contributors).
The GitHub UI can be used. Review the changes and
git merge --no-ff <branch>
