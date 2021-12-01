
# guidelines

## contributing issues
The issue tracker is the preferred channel for [bug reports](#bug-reports)
and [submitting pull requests](#pull-requests),
but please standard rules apply:

* Please **do not** use the issue tracker for personal support requests (use
  [Stack Overflow](http://stackoverflow.com)).

* Please **do not** derail or troll issues. Keep the discussion on topic and
  respect the opinions of others.

## bug reports

A bug is a _demonstrable problem_ that is caused by the code in the repository.
Good bug reports are extremely helpful - thank you!

Guidelines for bug reports:

1. **Use the GitHub issue search** &mdash; check if the issue has already been
   reported.

2. **Check if the issue has been fixed** &mdash; try to reproduce it using the
   latest `master` or development branch in the repository.

3. **Isolate the problem** &mdash; create a [reduced test
   case](http://css-tricks.com/reduced-test-cases/).

A good bug report shouldn't leave others needing to chase you up for more
information. Please try to be as detailed as possible in your report. What is
your environment? What steps will reproduce the issue? What would you expect to be the outcome?
All these details will help us to fix any potential bugs.

**Example:**

> Short and descriptive example bug report title
>
> A summary of the issue and the environment in which it occurs. If
> suitable, include the steps required to reproduce the bug.
>
> 1. This is the first step
> 2. This is the second step
> 3. Further steps, etc.
>
> Maybe an image attachment of the bug, if visual.
>
> Any other information you want to share that is relevant to the issue being
> reported. This might include the lines of code that you have identified as
> causing the bug, and potential solutions (and your opinions on their
> merits).


## pull requests

Good pull requests - patches, improvements, new features - are a fantastic
help. They should remain focused in scope and avoid containing unrelated
commits.

Traditionally, PR's to this repo are *expected* to be
either a new WSL distro or a bug fix to an existing WSL distro configuration. It's up to *you* to make a strong
case to convince us of the merits of your addition.

**Please ask first** before embarking on any significant pull request (e.g.
implementing features, refactoring code),
otherwise you risk spending a lot of time working on something that the
project's developers might not want to merge into the project.

Follow this process if you'd like your work considered for inclusion in the
project:

1. [Fork](http://help.github.com/fork-a-repo/) the project, clone your fork,
   and configure the remotes:

   ```bash
   # Clone your fork of the repo into the current directory
   git clone https://github.com/<your-username>/wsl/
   # Navigate to the newly cloned directory
   cd ctfbot
   # Assign the original repo to a remote called "upstream"
   git remote add upstream https://github.com/KNOXDEV/wsl/
   ```

2. If you cloned a while ago, get the latest changes from upstream:

   ```bash
   git checkout main
   git pull upstream main
   ```

3. Create a new topic branch (off the main project development branch) to
   contain your feature, change, or fix:

   ```bash
   git checkout -b <topic-branch-name>
   ```

4. Commit your changes in logical chunks. Please adhere to these [git commit
   message guidelines](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
   or your code is unlikely be merged into the main project. Use Git's
   [interactive rebase](https://help.github.com/articles/interactive-rebase)
   feature to tidy up your commits before making them public.

5. Locally merge (or rebase) the upstream development branch into your topic branch:

   ```bash
   git pull [--rebase] upstream <dev-branch>
   ```

6. Push your topic branch up to your fork:

   ```bash
   git push origin <topic-branch-name>
   ```

7. [Open a Pull Request](https://help.github.com/articles/using-pull-requests/)
   with a clear title and description.

**IMPORTANT**: By submitting a patch, you agree to allow KNOXDEV to
license your work under the "Unlicense" licence.