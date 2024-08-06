# Nocheckin

A simple git hook that rejects any attempts to
create a commit containing the phrase "nocheckin".

## Dependencies
- grep

## Install
### Per-repo
Place the `nocheckin` file in the `.git/hooks/` directory of
the repository that you want it to apply to,
and rename the file to `pre-commit`.

### For all new repos
Instead of the `.git/hooks/` directory of a repo like above,
rename the file and place it in `~/.git-templates/hooks/`.

Run the following command to tell Git where the template is located:
```bash
git config --global init.templateDir "~/.git-templates"
```

Any newly-created repos will have the nocheckin hook applied to them.

For existing repos, the `pre-commit` file will still have to
be placed somewhere in the project.
