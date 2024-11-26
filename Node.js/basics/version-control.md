# Version Control 101

## Resources _(Choose one for each topic)_

* Intro to Version Control
    - [Tarek Alabd](https://www.youtube.com/watch?v=AI6gw4HhZ8U)
    - [Yahia Tech](https://www.youtube.com/watch?v=HQb-FMBfjw4)
    - [Simplilearn](https://www.youtube.com/watch?v=Yc8sCSeMhi4)
* Git & GitHub
    - [Elzero Web School](https://www.youtube.com/playlist?list=PLDoPjvoNmBAw4eOj58MZPakHjaO3frVMF)
    - [Ghareeb Elsheikh](https://www.youtube.com/watch?v=fDkR0TDR9dI&t=2226s)
    - [freeCodeCamp](https://www.youtube.com/watch?v=RGOj5yH7evk&pp=ygUTZ2l0aHViIGZyZWVjb2RlY2FtcA%3D%3D)
    - [Big Data Arabic](https://www.youtube.com/watch?v=Q6G-J54vgKc)
* Markdown
    - [Web Dev Simplified](https://www.youtube.com/watch?v=_PPWWRV6gbA)
* Commit Messages
    - [Yallacode](https://www.youtube.com/watch?v=XMqPHAq4xkQ)
    - [Cameron McKenzie](https://www.youtube.com/watch?v=Kz2iyskwLRA)
* Conventional Commits & Semantic Versioning
    - [DevInsideYou](https://www.youtube.com/watch?v=JlfCRlFHmd8)

## Task

* SVN is a well-known version control system other than git. Compare between SVN and git according to:
    - Synchronization
    - Branching
    - Ecosystem

* Which of these statements in **NOT** correct? and why?
    - Git Bash provides Unix-like command line environment to windows users.
    - Git is a cloud-based service to store remote repositories.
    - `.gitignore` file contains paths that shouldn't be tracked by Git.
    - GitHub allows contributions of multiple developers on a single repository.

* Create a schedule of your faculty lectures using markdown tables.

* Write the git commands needed for each of the following scenarios:
    - You want to add all modified files to git staging without specifying each one of them.
    - You have a local repository and you need to add a remote with name `deploy` and url `https://git.heroku.com/example-app.git`.
    - You want to get the history of commits in the repository where each commit is represented by one line.
    - You try to make a commit but git asks you to enter your name and email first.
    - Your work is present on the branch `feature/chat` and you want to merge it with the branch `development`.
    - You realize that you want to add one more file to the last commit without creating a new commit.

* What does the `HEAD` keyword refer to in git?

* What are the problems with this commit message? list all what you notice.
    
    ### Commit message:
    Big change to fix everything that was broken

    ### Commit body:
    So I did a lot of stuff in this commit, including fixing bugs, adding new features, and refactoring code. Also cleaned up some old files. Not sure what exactly I did, but everything works now. Hope this doesn't break anything else. If it does, we'll just fix it later. Also, added some random changes to the config file, because why not? Should be good now. Oh, and I made a minor tweak to the UI, but I didn't check it fully. I think it's fine though. Whatever.

* I recently created [a new repository](https://github.com/saifsweelam/names-server), but it's still missing some things. I need you to contribute to it using pull requests. Fork the repository, do the following changes in order and then submit a pull request to my repository.
    - Fix the typo in the function name `getNamas()`
    - Move the two functions using file system to a separate module
    - Add the `node_modules` directory to a `.gitignore` file
    - Add a start script and a development script that uses nodemon
    - Add the functionality to delete a name from the list using the URL `/delete?name="Ahmed Mohsen"`.
    - Update the `README.md` file to include more details about the project

    Make sure to keep the following in mind:
    - Make separate changes in separate commits. Don't mix up stuff.
    - Use commit messages that follow standard rules and apply conventional commiting.
    - Describe all the changes you made in the pull request description.