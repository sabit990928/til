Ignore local files

- put needed files into .gitignore
- then `git update-index --assume-unchanged .gitignore`

_Update:_

To get undo/show dir's/files that are set to assume-unchanged run this:

`git update-index --no-assume-unchanged <file>`

To get a list of dir's/files that are assume-unchanged run this:

`git ls-files -v|grep '^h'`
