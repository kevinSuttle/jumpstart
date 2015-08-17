Jumpstart
==
Open source repository kit, designed for on-boarding new teammates.

**Goals:**
- Get new teammates up and running as fast as possible. Under 30 seconds should be the goal (minus dependency installation)
- Minimize the number of questions by practicing empathy, and continuously improving (don't fear change)
- Use tools to automate as much objectivity as possible, leaving subjectivity up to personal or group discussion.

## Files every repo needs
### README.md
- what the project is
- Link to where people who work on this project discuss it (Slack, etc.)
- Link to where the graphical assets are kept? (Box, wiki, etc.)

### [Contributing.md](https://github.com/blog/1184-contributing-guidelines)

- How to set up a local environment in 30 seconds
 - If you have to ask someone for access, something is wrong
- Git workflow docs
 - Code review process
 - CI/CD and testing process (It's a good idea to include a [badge](https://github.com/boennemann/badges) as well)
 - Criteria for pull request acceptance
- Add a section on configuration, including links to plugins for various IDEs/code editors, e.g. [.editorConfig](http://editorconfig.org/).

### [LICENSE file](https://help.github.com/articles/open-source-licensing/)
 - Most of the time, [MIT](http://choosealicense.com/licenses/mit/) is best for open-source projects, though companies may want to choose a more specific one, or rules for different use cases.

### APIs
Using an API? **Do not put secret keys in your source code repo.**
I _very strongly_ suggest [Vault](https://vaultproject.io/).  

### Front-end Specific
If you're working on front-end assets, you'll probably at least need these 3 files or something equivalent.

- [gulpfile.js](http://gulpjs.com/)
- [.eslintrc](http://eslint.org)
- [sass-lint.yml](https://www.npmjs.com/package/sass-lint)
