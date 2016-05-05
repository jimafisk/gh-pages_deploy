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
