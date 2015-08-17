_Below is an example of real contributing doc I used in an IBM Bluemix project. Modify it and make it your own._

## Homework
* [Naming things real good](https://cloudup.com/cw8cv3gW9-8)
* [Flow like GitHub](http://scottchacon.com/2011/08/31/github-flow.html)
* [Just watch this](https://www.youtube.com/watch?v=qyz3jkOBbQY)
* [5 useful tips for a better commit message](https://robots.thoughtbot.com/5-useful-tips-for-a-better-commit-message)

## Dev Environment
Make sure you're in the right CloudFoundry org and space by setting the following in your CLI.
`cf target -o ["$YOUR_ORG_NAME_HERE"] -s "[$YOUR_SPACE_NAME_HERE]"`

### Recommended Sublime Setup
Make sure you have [Package Control](https://packagecontrol.io/installation#st3) installed, and the [latest Sublime Text 3 Build](https://www.sublimetext.com/3).

#### Packages
Bring up the Command Palette with <kbd>⌘⇪p</kbd>, and choose *'Package Control: Install Package'*.

Then, install these packages.
<pre>
<kbd>
BracketHighlighter
CSS3
Dustbuster
EditorConfig
Emmet
Emmet CSS Snippets
GitGutter
HTML5
List stylesheet variables
SCSS
SublimeLinter
SublimeLinter-contrib-eslint
SublimeLinter-contrib-scss-lint
Syntax Highlighting for Sass
Trailing​Spaces
</kbd>
</pre>

#### Preferences
Make sure your EditorConfig and local preferences aren't overriding each other. [Here are mine](https://github.com/kevinSuttle/sublime-prefs/blob/master/Preferences.sublime-settings#L49) as an example.

## Pull request process
Any discussions about existing issues, commits, PRs, lines of code, etc. should be linked to. Usually this just means pasting a URL to the content being referenced. Sometimes there are shortcuts, like [closing issues in commit messages automatically](https://help.github.com/articles/closing-issues-via-commit-messages/).

### Requester
When you submit your PR, get 2 separate `:thumbsup:`👍🏼 before merging into master. The `:rocket:` 🚀 is meant to mean _"ship it!"_, but `:shipit:` is a GitHub-specific Emoji— a squirrel wearing a fedora. I thought a rocket made more sense (launch, rocket **ship**, deploy, you see where I'm going), but if the team likes the squirrel, then who am I to judge?

#### Check the merge message
Make sure to confirm the merge will be successful. If it's green, no worries.
![successful merge message](https://cldup.com/o7SkeSA9b6.png)

If it's grey, you'll see a message saying "We can't automatically merge this pull request". That usually means a merge conflict. Alert the requester in the PR comments. Maybe use a `:no_entry_sign:` 🚫.

![merge conflict message](https://cldup.com/Mv_JU842dS.png)

#### If it's good
1. Merge your branch
2. Delete your branch on GitHub (the button appears on the PR merge page)
3. On your local machine
	* `git checkout master`
	* `git pull`
	* `npm run deploy` (we have a manifest.yml that saves you typing)
	* delete your local branch

#### If there are problems
1. Make fixes on the same local branch
2. Push new commits to the same remote branch
3. Make sure the merge message is green.
4. Comment, asking the issue reporter to re-test. I don't have an Emoji for this. Maybe `:arrows_counterclockwise:` 🔄

#### If it's sitting too long
Add a comment on the PR `:hourglass_flowing_sand:`⌛️

### Reviewer
Check out the [PR locally](https://help.github.com/articles/checking-out-pull-requests-locally/), and **try to break it**. Test every scenario you can think of, after testing that the PR description and commit messages do what the requester says.

#### If you encounter an issue (_link to your repo's issues here_):
* confirm it hasn't [already been filed](https://github.com/cloud-platform-design/cloud-platform-beta/issues)
* Document it in a new issue
* Use the appropriate labels
* Use the appropriate milestone
* Assign the person whose PR you reviewed

#### If all is well, and the patch works:
* Comment with a 👍🏼
* If you're the 2nd 👍🏼, throw a 🚀 in there to let the reviewer know it's good to ship.
