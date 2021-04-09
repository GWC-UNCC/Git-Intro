# Hugo Specific

This is a section for hugo specific important parts, pertaining to git.

- [Hugo Specific](#hugo-specific)
  - [Sub-Modules](#sub-modules)
    - [Add a sub-module theme](#add-a-sub-module-theme)
    - [Remove a theme](#remove-a-theme)
    - [Update theme to most recent version](#update-theme-to-most-recent-version)
    - [Pull submodules after clone](#pull-submodules-after-clone)

## Sub-Modules

These are used when adding hugo themes, and while they are a very complex topic to cover.
We will only cover the bare minimum parts relevant to hugo, and you cannot use vscode for this.
You will have to use the CLI.

### Add a sub-module theme

This will be used to add themes to your hugo project.

```git
git submodule add <theme_git_url> themes/<name>
# i.e.
#   git submodule add https://github.com/themefisher/academia-hugo.git themes/academia-hugo
```

### Remove a theme

```git
git submodule deinit -f themes/<name>
git rm -f themes/<name>
# i.e.
#   git submodule deinit -f themes/academia-hugo
#   git rm -f themes/academia-hugo
```

### Update theme to most recent version

```git
git submodule foreach git pull origin master
```

### Pull submodules after clone

```git
git submodule update --init --recursive 
```

Now you should be ready to go to the next step of the [tutorial](/README.md#steps).
