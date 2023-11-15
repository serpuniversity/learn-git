# How to update all submodules from parent repository

1. Navigate to the parent directory
2. Run `git submodule update --recursive --remote`


**This command does the following:**

`--recursive`: This option ensures that the command applies not just to the submodules of the current repository, but also to any nested submodules inside those submodules, and so on, recursively.

`--remote`: This option tells Git to update the submodules to the latest commit in their respective remote repositories. Without this, the submodules would be updated to the commit currently referenced in the main repository.
