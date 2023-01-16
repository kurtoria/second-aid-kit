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

<!-- TODO: perhaps update if you need to do something else for private packages -->
## move from npm to github packages
1. Add this to your release script before "Create Release Pull Request or Publish"
```yml
- name: Creating .npmrc
    run: |
        cat << EOF > "$HOME/.npmrc"
        //npm.pkg.github.com/:_authToken=$GITHUB_TOKEN
        EOF
    env:
        GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```
2. Add config to package.json
```json
	"repository": {
		"type": "git",
		"url": "git+https://github.com/OWNER/REPOSITORY.git",
		"directory": "packages/PACKAGE_NAME"
	},
	"publishConfig": {
		"registry": "https://npm.pkg.github.com",
		"name": "@OWNER/PACKAGE_NAME",
		"directory": "./package",
		"access": "public" // TODO: maybe not of course?
	},
```
