# Jujutsu Test

This repo is made for playing with [Jujutsu VCS](https://github.com/jj-vcs/jj).

### Main Issues With Git

In real-world projects it is often the case that pull requests get quite big since developers tend to put too many things in one PR. There are multiple issues with big PRs:

- Reviewers tend to procrastinate tend to start reviewing later the more changes a PR has ([ref](https://graphite.dev/guides/github-pr-metrics#2-review-response-time) )
- There is more PR ping pong ([ref](https://graphite.dev/guides/github-pr-metrics#4-review-cycles-until-merge) )
- It requires much more concentration / focus to review bigger PRs.

I found a series of intersting blog posts regarding the big-PR topic:

- https://graphite.dev/blog/your-github-pr-workflow-is-slow
- https://graphite.dev/blog/how-large-prs-slow-down-development#measuring-the-impact-of-pr-scope

All of them more or less suggest **stacked branches**. Some teams already do that. But not regulary because mostly proper tooling is missing, since manually keeping stacked branches up to date is tedious. **But** the following tools look very promising:

| Name                                             | ⭐  |
| ------------------------------------------------ | --- |
| [JJ](https://github.com/jj-vcs/jj) 🔥            | 21K |
| [Git Town](https://github.com/git-town/git-town) | 3K  |
| [Sapling](https://github.com/facebook/sapling)   | 6K  |

### Jujutsu A Short Summary

I think after more than a decade of git it is time for a change. The VCS JJ looks very promsing and is also mentioned by some of the blogs when you dig deeper into this topic. It exceeds git in multiple points. You can read more about this [here](https://jj-vcs.github.io/jj/latest/git-comparison/).

> [!tip]
> `jj git init --colocate` will import an existing git repo into JJ. This enables to work side-by-side with Git and JJ ([ref](https://youtu.be/ou4ZNRFXkO0?si=8Z7L1eQ3SASDpusA&t=190)).

<!-- ==========================================================================================
BEGIN: AI Summary of JJ's README file
========================================================================================== -->

<details><summary>AI Summary of JJ's README file</summary>
<p>

#### 🌀 What is Jujutsu (“jj”)

- **Jujutsu** is a modern version control system designed for both simplicity and flexibility.
- It decouples **user-facing operations** from the underlying **storage backend**, allowing it to support multiple backends (e.g. Git, Mercurial, hybrid).
- By default it uses a **Git repository as its storage layer**, ensuring compatibility with existing Git tools.

#### ✨ Key design features & innovations

- **No explicit index / staging area** — there’s no separate “staging” step; changes are committed automatically (snapshot model).
- **Working copy as a commit** — the working directory is treated like a commit, so changes are integrated into the commit history seamlessly.
- **Operation log & undo support** — every operation (commit, pull, push, etc.) is recorded, making it easier to recover from mistakes.
- **Automatic rebasing & conflict propagation** — when you rewrite history, descendant commits are rebased automatically. Conflict resolutions are also handled and propagated.
- **Conflicts as first-class objects** — instead of being ephemeral, conflicts can be represented as persistent objects in history.
- **Concurrency safety** — the design is robust to uses like Dropbox, `rsync`, or concurrent replication, reducing risk of repository corruption.

#### 🚀 Current status & roadmap

- The **Git backend** is considered production-ready; other backends are under development.
- There are features still in progress, such as **Git submodule support**, performance optimizations, and broader workflow coverage.
- Some workflows or setups outside the core team’s style may not yet be fully supported.
- Upgrades to future on-disk formats will be handled via migrations or commands where necessary.

#### 🧩 Why use Jujutsu?

- You get many **Mercurial-like features** (revsets, anonymous branches) with Git compatibility.
- The UX is intended to be snappy, intuitive, and robust.
- Mistakes are easier to undo thanks to the operation log.
- Complex workflows like rewriting history become simpler and safer.

</p>
</details>

<!-- ==========================================================================================
END: AI Summary of JJ's README file
========================================================================================== -->

### Links

- 👨‍💻 Tutorial - [Google's Git Killer Is INSANELY Better (and it's open source)](https://www.youtube.com/watch?v=cZqFaMlufDY)
- 👨‍💻 Tutorial - [JJ With Git is My New Favorite Workflow](https://www.youtube.com/watch?v=ou4ZNRFXkO0)
- 👨‍💻 Tutorial - [Extensive Tutorial by Steve Klabnik](https://steveklabnik.github.io/jujutsu-tutorial/)
- 👨‍💻 GUI - [VisualJJ](https://www.visualjj.com/)
- 👨‍💻 Terminal - [Starship Prompt Support for JJ](https://github.com/starship/starship/issues/6076)
- 📚 Docs - [Comparison with Git](https://jj-vcs.github.io/jj/latest/git-comparison/)
- 📚 Docs - [Tutorial](https://jj-vcs.github.io/jj/latest/tutorial)
