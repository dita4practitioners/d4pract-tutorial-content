# DITA For Practitioners Tutorial Materials

Contains the source content and worked examples for the DITA for Practitioners tutorials, including the end-to-end authoring tutorial.

This project contains the step-by-step worked example reflecting each step in the tutorial. 

Major steps are represented by branches, one for each major step. Within each step, the individual steps are identified by git tags, i.e. branch "step-01" has all the commits that make up tutorial step 1, while each commit within step 1 is tagged as "step-01.01", "step-01.02", etc.

You can use these branches and tags to check out the repository to any point in the tutorial.

The head commit on the main branch reflects the final state of the tutorial.

## Using git work trees to compare tutorial steps

One interesting way to explore the tutorials is to use the git worktree feature (available since early 2020 versions of git) to check out different steps into separate directories, making it easy to compare two states in the tutorial.

For example, to create separate directories for steps 1 and 2, use these git commands, having cloned the repository initially.

```
% cd ~/workspace/dita4pract-tutorial-materials
% git worktree add ../tutorial-step-01 step-01
% git worktree add ../tutorial-step-02 step-02
```

This will create the directory `~/workspace/tutorial-step-01`, checked out to branch `step-01` and the directory `~/workspace/tutorial-step-02`, checked out to branch `step-01`.

You can get the list of work trees using the `git worktree list` command:

```
% cd ~/workspace/dita4pract-tutorial-materials
% git worktree list
/Users/ekimber/tutorial-step-01 136c7f3 [step-01]
/Users/ekimber/tutorial-step-02 4a6c52e [step-02]
%
```

All the work tree directories are associated with the git history managed in the initial clone directory (`~/workspace/dita4pract-tutorial-materials` in this example), so there is only one clone of the remote repository.

You can delete unwanted work trees using the `git worktree remove` command:

```
% cd ~/workspace/dita4pract-tutorial-materials
% git worktree remove ../tutorial-step-01
% 
```

This will delete the worktree directory if there are no uncommitted changes in the directory.