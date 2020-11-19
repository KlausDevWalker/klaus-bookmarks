# Klaus' Bookmarks
A repository for my bookmarks

## Steps to rewrite your own log

- Delete `.git` and other files and folders. Leave this folder with just the file and folders below:
```shell
drwxr-xr-x  2 git-hooks
-rw-r--r--  1 .gitignore
-rw-r--r--  1 .travis.yml
-rw-r--r--  1 commitlint.config.js
-rw-r--r--  1 LICENSE
-rw-r--r--  1 package.json
-rw-r--r--  1 README.md
```

- Edit some files that clearly show my info with yours, like this `README.md`, the `package.json` and all the config files themselves;

- Run the commands below to install `standard-version`, initialize the folder with `git`, generate a root empty commit, create a commit with the initial files, generate the first release and publish it up to the remote repository:
```shell
npm install -g standard-version

git init && yarn install && git commit --allow-empty -m "chore(*): create root commit" && git remote add origin git@github.com:KlausDevWalker/klaus-bookmarks.git && git add . && git commit -m "chore(*): create initial commit" && yarn run release --first-release && yarn run publish
```

## License

This repository is licensed under the GNU General Public License v3.0 License. See [LICENSE](LICENSE) for more information.
