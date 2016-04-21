- [Committing](#workflow)
- [Branching](#branching)
- [Merging](#merging)


<a id="workflow"></a>
## A Basic Git Commit Workflow

    git clone <project>
    
    git checkout -b feature/x dev    // New feature branch from dev branch (see Branching below)

    // Do your coding magic
    
    git add <file>

    git commit -m 'My changes'    // While working on my machine
    
        // <-- My colleague did a "git push" here
    
    git pull --rebase    // Before I can push, I need to rebase
    
    git push    // Now my changes are on top

<a id="branching"></a>
## Branching

- **master**
  - reflects a *production-ready* state
  - pushed to "prod"
- **dev**
  - reflects a state with the latest changes for the *next release*
  - branches from/into **master**
  - pushed to "staging"
- **feature/x**
  - branches from/into **dev**
  - contains full commits for a feature
- **release/x**
  - branches from/into **dev**
  - small edits, bug fixes, versioning, etc to prepare for a release
  - QC tickets, with ticket number in commit message
- **spike/x**
  - branches from/into **dev or current release/feature**
  - explore implementations that then become a feature or bug fix

In emergencies, break glass:

- **hotfix/x**
  - branches from/into **master**
  - fix immediate bugs in production code

<a id="merges"></a>
## Merges

- **DO NOT COMMIT CODE WITH MERGE CONFLICTS**
- Code should be reviewed by Lead Dev on project
- Changes should be fully understandable via commit messages/code comments
- Ticket numbers can be referenced in commit message
    - `git commit -m "re #601 fix header padding"`
- Merge performed by code reviewer

References:

* [Branching](http://nvie.com/posts/a-successful-git-branching-model/)
* [Commit workflow](http://kentnguyen.com/development/visualized-git-practices-for-team/)
