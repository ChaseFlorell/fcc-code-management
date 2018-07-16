## @color[orange](Code Management)

The purpose of this discussion is to bring alignment to our code management process across the various teams working on the AgExpert project line.

---

### @color[orange](Branches) 

**@fa[git]**

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