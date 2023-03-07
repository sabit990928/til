### git mv

Here are a few examples of using the git mv command to rename files in Git:

    Renaming a file in the same directory:

```shell
$ git mv old-file-name.txt new-file-name.txt
```

This command renames the file old-file-name.txt to new-file-name.txt in the same directory. Git tracks this as a single atomic operation, so you'll see a single commit in the repository history for the rename.

Moving a file to a different directory:

```shell
$ git mv file-to-move.txt new-directory/
```

This command moves the file file-to-move.txt to the directory new-directory/. Git renames the file and updates the file path in the repository, tracking this as a single atomic operation.

Renaming a directory:

```shell

    $ git mv old-directory/ new-directory/
```

    This command renames the directory old-directory/ to new-directory/. Git updates the file paths for all files within the directory, tracking this as a single atomic operation.

Using the git mv command can help ensure that Git tracks file renames correctly, preserving the history of the codebase and making it easier to understand changes over time. It's also worth noting that you can use git mv to move and rename files in the same operation, such as:

```shell

$ git mv old-file-name.txt new-directory/new-file-name.txt
```

This command moves the file old-file-name.txt to the directory new-directory/ and renames it to new-file-name.txt. Git tracks this as a single atomic operation, preserving the file history and making it easy to understand the codebase changes.
