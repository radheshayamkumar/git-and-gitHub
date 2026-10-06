🌿

# Git Branching

## Part 2: Parallel Universe of Code

Main ko haath mat lagao, apni branch banao! 😎

Tap Next or press the → key to start.

## What is a branch?

A **branch** is a separate line of work. You can try new things safely, and the stable code stays untouched. When you are happy, you **merge** it back.

`git branch` → list branches\
`git checkout -b dev` → create **and** switch (`-b` = new)\
`git switch dev` → switch (modern way)\
`git switch -c dev` → create and switch

**HEAD** = the latest commit of the branch you are on.\
`git log --oneline` shows it.\
Branches share history up to the split point. After that, each branch gets its own new commits.

Note: the default branch is now usually `main`. Older setups still say `master`. Same idea, new name.

Branch = apna alag room, main = drawing room 🛋️

## Watch a branch live 🎬

Split karo, kaam karo, merge karo!

## Branching strategy 🏗️

🌱 **feature/ticket-ID**\
one per feature, made from dev

➜

🧪 **dev**\
developers combine features

➜

🔍 **staging / QA**\
testing

➜

🚀 **main**\
protected, production

🚑 **Bug in production? Make a `hotfix` branch** from main. Fix it, merge into **main** and also into **dev** (so the fix is not lost). Then staging gets it through the normal flow.

50 developers on 50 features = 50 feature branches. This style comes from the "Git Flow" model (nvie.com). Small teams may also use simpler trunk-based development.

Production ek mandir hai, seedha jootey mat pehno! 🛕

## Merge in practice 🔀

`git switch -c dev`\
`git switch -c staging`\
(on dev) create `features.md`, add, commit\
`git switch staging`\
`git merge dev`\
`git log --oneline`

💥 **Merge conflict**: two people changed the same line.\
Git marks it with `<<<<<<<` `=======` `>>>>>>>`.\
Edit the file, keep the right code, then `git add .` and `git commit`.

Merging into main: do it on GitHub with a Pull Request, so teammates can review first. Git alone has no review step.

Do cook, ek dish mein namak = conflict! 🧂😅

## Cheat sheet 📋

| `git branch` | List branches |
| --- | --- |
| `git switch -c name` | Create and switch |
| `git switch name` | Switch branch |
| `git merge name` | Merge it into the current branch |
| `git log --oneline` | Short history, shows HEAD |

Next: Part 3, GitHub: clone, push, pull, SSH 🔑

1 / 6