# Nocheckin

A simple git hook that rejects any attempts to
create a commit containing the phrase "nocheckin".

## Install
### Per-Repo, Local Machine
Place the `pre-commit` file in the `.git/hooks/` directory of
the repository that you want it to apply to.


### Per-Repo, All Collaborators
Place the `pre-commit` file in a directory of your choosing,
within the target repo (eg: `project/.githooks/`).

Configure the repo to look in this directory for hooks, if you haven't done so already:
```bash
git config --local core.hooksPath .githooks
```

### Local Machine
Place the `pre-commit` file somewhere in your home directory,
eg. `~/.config/git/hooks`

Configure git to use this directory for hooks globally:
```bash
git config --global core.hooksPath ~/.config/git/hooks
```

### Only New Repos
Instead of the `.git/hooks/` directory of a repo like above,
place it in `~/.git-templates/hooks/`.

Run the following command to tell Git where the template is located:
```bash
git config --global init.templateDir "~/.git-templates"
```

Any newly-created repos will have the no-checkin hook applied to them.

For existing repos, the `pre-commit` file will still have to
be placed somewhere in the project.
