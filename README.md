# git-hooks

Some useful git hooks

## Usage

### Adding as a submodule

The recommended way to use these hooks is to add this repository as a submodule within your git repository...

```bash
git submodule add git@github.com:rconway/git-hooks
```

...and commit the resulting files `.gitmodules` and `git-hooks` to your repository.

### Cloning your repos with the submodule

Subsequent clones of your repository should be made with the `--recurse-submodules` option to ensure initialisation of the `git-hooks` submodule...

```bash
git clone --recurse-submodules <your-repos-url>
```

Alternatively, the initialisation of the submodule can be made after main repos clone...

```bash
git submodule update --init
```

### Installing the hooks from the submodule

To install the hooks into your main repos .git/hooks directory run the script...

```bash
./git-hooks/install-hooks.sh
```

NOTE that this install script assumes that your main repos `.git` directory is sibling to the `git-hooks` submodule directory.
