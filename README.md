# gh-pages_deploy
Uses a pre-push git hook to deploy compiled assets from a jekyll project to gh-pages for static site hosting

## Setup
1.) Download "pre-push" file from this repository<br />
2.) Put "pre-push" file in the hooks directory of your git enabled project so it appears like so:<br />
    `.git/hooks/pre-push`<br />
3.) Make sure the script is executable:<br />
    `chmod u+x .git/hooks/pre-push`<br />
4.) Make sure your _site folder is being tracked by commenting out or removing the "_site" line in your .gitignore file<br />
5.) Make changes to your Jekyll project<br />
6.) Compile your static site assets by running `jekyll serve`<br />
7.) Add and commit changes<br />
8.) Push your master branch via the terminal and you should be prompted whether or not to deploy (input "y" for yes).

**Note 1:** If you don't already have a `gh-pages` branch on your remote repo, you might get an error like this:
```
error: unable to push to unqualified destination: gh-pages
The destination refspec neither matches an existing ref on the remote nor
begins with refs/, and we are unable to guess a prefix based on the source ref.
error: failed to push some refs to 'git@github.com:yourorg/yourproject.git'
```
You should manually create a new branch on Github (Just click on where it says <kbd>Branch: master</kbd> in the top left of your repository, start searching for `gh-pages` and it will prompt you to create a new branch with that name).

**Note 2:** If you just created a new `gh-pages` branch on github, it will contain all the project files, and not just the built assets, so you may need to add the `--force` flag to do your initial push.

**Note 3:** If using fishshell, replace the backtick characters " \` " with paranthesis " ( ". Example: `git push origin (git subtree split --prefix _site master):gh-pages --force --no-verify`
