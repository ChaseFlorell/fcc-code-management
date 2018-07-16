## @color[orange](Code Management)

The purpose of this discussion is to bring alignment to our code management process across the various teams working on the AgExpert project line.

*note: this is meant to be a discussion, please provide feedback and opinions as you see fit.*

---

### @color[orange](Branches) 

###### @fa[git] 

As of last week, we are no longer using the @color[red](mobile/development) branch. All teams are now focusing their efforts on the `developement` branch. New branching structure is as follows

@fa[arrow-down]

+++

@transition[slide]

### @color[orange](Branches cont..)

 @color[red](master)
    
  - currently released into production
  - each release will also get tagged with the released version
  - only hotfixes are created off of this branch

@fa[arrow-down]

+++

@transition[slide]

### @color[orange](Branches cont..)

 @color[red](release/[N.N]) @color[](where N.N is the release version)
 
  - work staged for the upcoming release
  - this branch is feature complete
  - only bug fixes once this branch is created
  - any developer PRing to this branch is responsible to also PR to @color[red](development)

@fa[arrow-down]

+++

@transition[slide]

### @color[orange](Branches cont..)

 @color[red](development)

  - all remaning work happens here
  - feature branches are created off of this branch

---

### @color[orange](Commits)

Keeping your code manageable starts with your commits. It's important to commit early and commit often and keep your commits small. A single file commit is best, but at minimum, keep your commits to a single topic. It's ok to have many commits in a single Pull Request.

@fa[arrow-down]

+++

@transition[slide]

### @color[orange](Commit Messages)

Commit messages are equally as important. By adding your task/bug/issue number in your commit message, VSTS can reference it in your story as well as your pull request. It also makes it easier to track down code changes from within the story card. When you add your issue number to your commit message, the story will become automatically referenced in your Pull Request.

---

### @color[orange](Pull Requests)

Keeping your PRs small is extremely important to code quality. If a given reviewer is going to give you 5 minutes of their time for a code review, that 5 minutes spent on a huge PR will inevitably cause a drop in quality.

Submitting a single PR per Task will result in your code being easier to review and understand.