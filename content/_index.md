+++
title = "Git Underneath"
+++
<!--: .wrap .size-80 ..alignright bgimage=images/welcome.gif -->

# **G I T**
# **U N D E R N E A T H**
---

<!--: .wrap .aligncenter -->

# What is GIT? {.text-landing}

---


<!--: .wrap .aligncenter -->

# How Git Records Changes ? {.text-landing}

---


<!--: .wrap -->

- Git stores snapshot as object inside your .git directory, Which structure look like this.

```
.git
├── HEAD
├── config
├── hooks
├── objects
│ ├── info
│ └── pack
└── refs
 ├── heads
 └── tags
```
- Git stores most of the content inside **`Objects`** directory. If you go inside this directory **`.git/objects/`** it will have folders which records different snapshot.
- While **`.git/objects/info`** contains information regrading file that are excluded, where as **`.git/objects/pack`** contains all objects that are removed.
- **`HEAD`** represents refs, current branch which it is referring.
- **`config`** will hold your configuration which will be repository specific.
- **`hooks`** it contains scripts to be executed on trigger of particular event.
- **`refs`** have **`head`** & **`tag`** folders respectively, where **`head`** represents current commit pointed in each branch that you have worked and **`tag`** contains the information about tag that you have created.
---

<!--: .wrap .aligncenter -->

# What are the  {.text-landing}
# types of Git **Merge** ? {.text-landing}

---

<!-- : .wrap -->

|||v

### **Merge**

A standard merge will take each commit in the branch being merged and add them to the history of the base branch based on the timestamp of when they were created. It will also create a merge commit, a special type of “empty” commit that indicates when the merge occurred.


![merge-meme](images/git-merge-git.gif "merge-meme")

|||


![merge](images/git-merge.png "merge")

---

<!-- : .wrap -->

|||v

### **Fast Forward Merge**

No new commits were made to the base branch since our branch was created, Git can do something called a “Fast Forward Merge”. This is the same as a Merge but does not create a merge commit. This is as if you made the commits directly on the base branch. The idea is because no changes were made to the base branch there’s no need to capture a branch had occurred.


![fast forward merge](images/fast-forward.gif "fast forward merge")

|||

![fast forward merge](images/git-fast-forward.png "fast forward merge")


---

<!-- : .wrap -->

|||v

### **Squash & Merge**

Squash takes all the commits in the branch (A,B,C) and melds them into 1 commit. That commit is then added to the history, but none of the commits that made up the branch are preserved.


![squash and merge](images/git-squash.gif "squash and merge")

|||

![squash and merge](images/git-squash.png "squash and merge")


---

<!-- : .wrap -->

|||v

### **Rebase & Merge**

A rebase and merge will take where the branch was created and move that point to the last commit into the base branch, then reapply the commits on top of those changes.This is like a fast forward merge, but works when changes have been made into the base branch in the mean while


![rebase and merge](images/git-rebase.gif "rebase and merge")

|||

![rebase and merge](images/git-rebase.png "rebase and merge")


---

<!--: .wrap .aligncenter -->

# Let's do some exercise.
![exercise](images/excercise.gif "exercise")

