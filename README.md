# gh-pages_deploy
Uses a pre-push git hook to deploy compiled assets from a jekyll project to gh-pages for static site hosting

## Setup
1.) Download "pre-push" file from this repository<br />
2.) Put "pre-push" file in the hooks directory of your git enabled project so it appears like so:<br />
`.git/hooks/pre-push`<br />
3.) Make sure the script is executable:<br />
`chmod u+x .git/hooks/pre-push`<br />
4.) Make changes to your Jekyll project then push your master branch and input "y" for yes when prompted
