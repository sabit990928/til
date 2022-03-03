## git patch

Shortly, maybe will add details later.

You can run `git format-patch "branch_name_to_differentiate_commits"`. For example when you branch has 6 commits ahead of master, then this command will be like `git format-patch master`. It will generate 6 patch files. That command has other options to save files in directory which you like, etc.

Vise versa you can apply that changes by running `git am "patch_file"` and it will show up in commit history.

In my case it showed up some conflicts, but you can run `git am -3 < "/path_patch"`, which makes some merge manipulations that ignore whitespaces, etc and show you only real conflicting cases, that could be solved with usual `--continue`, `--abort`.

More details: [devconnected](https://devconnected.com/how-to-create-and-apply-git-patch-files/), [stackoverflow](https://stackoverflow.com/questions/16190387/when-applying-a-patch-is-there-any-way-to-resolve-conflicts).
