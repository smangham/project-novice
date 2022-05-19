---
title: "Managing a Mini-Project"
slug: project-novice-managing-a-mini-project
teaching: 0
exercises: 20
questions:
- "How do we put everything we've learnt together?"
objectives:
- "Go through the steps of managing a small software project."
keypoints:
- "Problems with code and documentation can be tracked as issues."
- "Issues can be managed on a project board."
- "Issues can be fixed using the feature-branch workflow."
- "Stable versions of the code can be published as releases."
---

Now we've seen all the steps involved in developing sustainable code, let's put that knowledge into practise.

Earlier, we made a fork of the `project-novice-demo` repository. The code there is pretty bad - it's written in a very unsustainable way that makes future development harder (and passing the project on to another researcher even harder!). However, as a published project owned by somebody else, we don't have the permissions required to edit it and fix the problems.

Fortunately, we have already forked it, and now we're going to set up a small project to improve it.
We'll use the tools we've introduced in this lesson so far. Forks don't have **Issues** by default, but you can enable them by going to  the **Settings** tab, then scrolling down to **Features**:

![Selecting the settings tab](fig/06-project/project-settings.png)
![Enabling issues](fig/06-project/project-settings-issues.png)

Now we can start looking for problems with the project and recording them as issues. One immediate one is that there's no `develop`/`dev` branch - all the work has been done on the `master` branch:

![No dev branch](fig/06-project/project-settings.png)

{: .challenge}
> ## Identifying issues
> We've found one problem, but there's *plenty* more here. Take a look at your fork of the `project-novice-demo` repository, identify two more things wrong with the code, and raise them as issues. Don't try to run the code - there's more than enough things wrong with it that you can spot just from a quick read-through.
> Once you've got your issues, create a kanban board on the repo and place them on it.

{: .solution}
> ## Solution
>
> There's too many things wrong to provide an exhaustive list, but here's a few you may have spotted:
> * No stable releases
> * Unclear commit messages
> * `LICENSE.md` is empty
> * `README.md` has an inaccurate list of files
> * `README.md` contains broken links
> * `What questions do we want to answer with this data?` is unfinished
> * Multiple versions of the same file in the repository
> * Poorly-named functions (e.g. `add_column5`)
> * Poorly-named variables (e.g. `df47`)
> * Poorly-documented functions *(e.g. `plot_bar_charts`)
> * Undocumented functions (e.g. `produce_count`)

Now we'll work on addressing the issues we've raised. If we want to use the feature-branch workflow, the lack of a `dev` branch is the first one we need to fix! So we'll fix that first.

{: .challenge}
> ## Solving problems
> 
> Now we've got a `dev` branch and a project board with a To Do column with issues in, we can set about fixing one of them.
> 
> We want to use the feature-branch workflow, so it would be easy to collaborate with other people. Pick one of your open issues, and fix it using the feature-branch workflow, then once it's done issue a release of your updated `master` branch!
>
> If you don't have any issues that can be fixed with the feature-branch workflow (e.g. *'Unclear commit messages'*) then add a new issue that the code has an inaccurate list of files in `README.md`, and work on fixing that.

{: .solution}
> ## Solution
>
> In order to address the issue we chose, we'll need to do the following:
> * Move our issue from To Do to Work In Progress
> * Select our `master` branch, and create a `dev` branch coming off it
> * Select our `dev` branch, and create a new issue branch coming off it- you could call it `issue_<problem_description>` or similar
> * Switch to our issue branch, fix the issue, commit our fixes and push them
> * Submit a pull request from our issue branch to `dev`
> * Close our issue on GitHub
> * When `dev` is up to date, submit a pull request from `dev` to `master`
> * When `master` is up to date, issue a release on GitHub
>
> Normally, we wouldn't just merge a branch into `dev` then `dev` straight into `master`- we'd merge several fixes or new features into `dev`, then merge to `master` and make a release. 


Now you should have a good idea of the skills and techniques required to manage a project successfully!

{% include links.md %}
