# Git Notes --- Beginner to Advanced

A beginner-friendly Git reference covering everyday commands, branching,
collaboration, recovery, and advanced workflows, with examples relevant
to embedded C and firmware projects.

## Main document

**Word document:** `Git_Notes_Beginner_to_Advanced_FINAL.docx`

Keep this README in the same folder as the Word document so the purpose
and contents of the notes are easy to find.

## What is covered?

-   Git fundamentals and repository setup
-   `git init`, `git clone`, configuration, status, staging, and commits
-   Viewing history and changes with `git log`, `git diff`, and
    `git show`
-   Branch creation, switching, merging, rebasing, and cherry-picking
-   Remotes, `fetch`, `pull`, `push`, and upstream tracking
-   Command options and terms such as `-m`, `-b`, `--global`, `origin`,
    `main`, `HEAD`, and `upstream`
-   Merge conflicts and how to continue or abort a merge/rebase
-   Undoing and recovering changes with `restore`, `reset`, `revert`,
    and `reflog`
-   Tags, releases, stashing, hooks, submodules, `.gitignore`, and
    `.gitattributes`
-   Debugging tools such as `git bisect` and `git grep`
-   Team workflows, Pull Requests, and firmware repository practices
-   Troubleshooting tables and quick-revision workflows

## Recommended learning path

1.  **Beginner:** Learn repository basics, `status`, `add`, `commit`,
    `log`, and `diff`.
2.  **Intermediate:** Practice branches, merge, remote repositories,
    `fetch`, `pull`, and `push`.
3.  **Collaboration:** Learn feature branches, upstream tracking, Pull
    Requests, and conflict resolution.
4.  **Recovery:** Understand `restore`, `reset`, `revert`, and `reflog`
    before using destructive commands.
5.  **Advanced:** Study rebase, cherry-pick, bisect, worktrees, hooks,
    and release tags.

## Daily workflow

``` bash
git status
git diff
git add <file>
git diff --staged
git commit -m "Describe the change"
git push
```

For a new branch, a typical start is:

``` bash
git switch -c feature/your-change
```

For its first push, if `origin` is the correct remote:

``` bash
git push -u origin feature/your-change
```

Use your team's workflow and branch policies where they differ from
these examples.

## Important safety notes

-   Review `git status` and `git diff` before changing or discarding
    files.
-   `git reset --hard` can discard uncommitted changes.
-   Force-pushing rewrites remote history. Prefer `--force-with-lease`
    only when a history rewrite is required and it is approved.
-   Do not commit passwords, access tokens, private keys, or other
    secrets. If a secret is pushed, revoke/rotate it; deleting it in a
    later commit does not make it safe.
-   Resolve conflicts carefully and build/test the project before
    completing a merge or rebase.
-   Git options are command-specific. Check the installed version with
    `git help <command>` or `<command> -h`.

## Quick glossary

  -----------------------------------------------------------------------
  Term                                Meaning
  ----------------------------------- -----------------------------------
  Repository (repo)                   A project tracked by Git

  Commit                              A saved snapshot of staged changes

  Branch                              A movable name pointing to a commit

  Remote                              A named connection to another
                                      repository

  `origin`                            A common default remote name, not a
                                      Git command

  `main`                              A common branch name, not a
                                      guaranteed name

  `HEAD`                              Usually identifies the currently
                                      checked-out commit/branch

  Staging area / index                The place where changes are
                                      selected for the next commit

  Pull Request (PR)                   A collaboration/review feature
                                      provided by hosting platforms, not
                                      a Git command
  -----------------------------------------------------------------------

## Scope

This README is a short guide to the companion Word notes; it does not
replace them or list every Git option. Git's available options depend on
the command and installed version. Confirm exact syntax with Git's
built-in help.
