# monorepo
Messing around with a monorepo.

## Adding new projects
### Option 1: as a subdirectory
```
uv init my_project
git add my_project
git commit -m "feat: add new demo my_project"
git push
```
### Option 2: as a submodule
```
git submodule add -b main git@github.com:path/to/my_project.git
git add .gitmodules my_project
git commit -m "feat: add new demo my_project"
git push
```
### Option 3: as a subtree
```
# Add the remote for the project repository
git remote add -f my_project_remote git@github.com:path/to/my_project.git

# Add the subtree, prefixed with the folder name you want
git subtree add --prefix=my_project my_project_remote main --squash

# Later, to pull changes from the project repository
# git subtree pull --prefix=my_project my_project_remote main --squash

# Or to push changes to the project repository
# git subtree push --prefix=my_project my_project_remote main
```
