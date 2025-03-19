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
