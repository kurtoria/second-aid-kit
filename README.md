# Second aid kit

Test repo for turborepo, release workflows and changesets.


## changeset
1. check out branch
2. do stuff you need
3. add changeset and follow promts
```bash
pnpm changeset
```
4. commit changeset
5. push and create pr
6. when cool beans - merge. Release workflow starts and checks for changeset, if there are any it will automatically create new PR versions updated.
7. When you are ready for a new release of the package - merge that pr and workflow will start again to check if versions been bumped and in that case release package to github packages
