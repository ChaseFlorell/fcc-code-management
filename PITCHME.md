## @color[orange](Code Management)

The purpose of this discussion is to bring alignment to our code management process across the various teams working on the AgExpert project line.

*note: this is meant to be a discussion, please provide feedback and opinions as you see fit.*

---

### @color[orange](Branches) 

As of last week, we are no longer using the @color[red](mobile/development) branch. All teams are now focusing their efforts on the @color[red](development) branch. New branching structure is as follows

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

 @color[red](release/[N.N]) *@color[white](where N.N is the release version)*
 
  - work poised for the upcoming release
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

Keeping your code manageable starts with your commits. 

It's important to commit early, commit often, and keep your commits small. A single file commit is best, but at minimum, keep your commits to a single topic. It's ok to have many commits in a single Pull Request.

@fa[arrow-down]

+++

@transition[slide]

### @color[orange](Commit Messages)

Commit messages are equally as important. By adding your task/bug/issue number in your commit message, VSTS can reference it in your story as well as your pull request. It also makes it easier to track down code changes from within the story card. When you add your issue number to your commit message, the story will automatically be referenced in your Pull Request.

@fa[arrow-down]

+++

@transition[slide]

### @color[orange](Commit Messages cont...)

Good practices for a commit message

 - helpful commit messages include describing what you've done and files that changed.
 - adding your initials to a commit message makes it easier to see code authors when scanning the commit log.
 
```
> git commit -m "[CF] (Issue #1234) meaningful message"
```

@fa[arrow-down]

+++

@transition[slide]

### @color[orange](Commit Messages cont...)

Unhelpful commit messages

```
git commit -m "I hate timezones"
git commit -m "fixed stuff"
```

---

### @color[orange](Keeping your branch current)

Keeping your branch current with the upstream branch will make everyone's life easier when it comes to combining your work with the rest. Just like committing early and often is important, it's equally important to rebase the source branch (typically  @color[red](development)) when you commit, or at least every couple of commits. 

*watching for completed PRs and rebasing at that point is also acceptable*

@fa[arrow-down]

+++

@transition[slide]

### @color[orange](Keeping your branch current cont...)

Merging vs Rebasing

 @fa[arrow-down] @fa[arrow-down] @fa[arrow-down]

+++

@transition[slide]

### @color[orange](Keeping your branch current cont...)
Merging literally merges two code bases together, this will create a merge commit in the process. Once a merge happens, the linear line of commits is broken, think of shuffling a deck of cards.

@fa[arrow-down]

+++

@transition[slide]

### @color[orange](Keeping your branch current cont...)

Rebasing will re-base your work on top of the source branch. In other words, your work will move to the front of the line and be based on the source.

@fa[arrow-down]

+++

@transition[slide]

### @color[orange](Keeping your branch current cont...)

The Golden Rule of Rebasing

Once you understand what rebasing is, the most important thing to learn is when not to do it. The golden rule of git rebase is to never use it on public branches.

Essentially, you can rebase your branch off of @color[red](development) but you **never** want to rebase @color[red](development) off of your branch.

@fa[arrow-down]

+++

@transition[slide]

### @color[orange](Keeping your branch current, example)

```
> git add .
> git commit -m "[CF] my meaningful message"
> git checkout development
> git pull origin development
> git checkout -
> git rebase development
> git push 
```

@[1,2](Commit your current work.) 
@[3,4](Update the working copy of your source branch.) 
@[5-7](Rebase on top of your source branch, and then push.)

---

### @color[orange](Pull Requests)

Keeping your PRs small is extremely important to code quality. 

> If a given reviewer is going to give you 5 minutes of their time for a code review, that 5 minutes spent on a huge PR will inevitably cause a drop in quality.

Submitting a single PR per Task will result in your code being easier to review and understand.

@fa[arrow-down]

+++

@transition[slide]

### @color[orange](Pull Requests cont...)

Good practices for a pull request

 - adding the size in the PR title helps reviewers know what they're in for.

 > [S] Added French translations for Field Details

  - when you begin reviewing ones PR, add a commit as such so that others know it's already being reviewed.

---

  ### @color[orange](Questions / Discussion...)

   - Daniel: discuss branch folders