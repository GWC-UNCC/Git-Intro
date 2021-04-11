# Hugo Specific

This is a section for hugo specific important parts, pertaining to git.

- [Hugo Specific](#hugo-specific)
  - [Sub-Modules](#sub-modules)
    - [Add a sub-module theme](#add-a-sub-module-theme)
    - [Clone Recursively](#clone-recursively)
    - [Pull submodules after clone](#pull-submodules-after-clone)
    - [Remove a theme](#remove-a-theme)
    - [Update theme to most recent version](#update-theme-to-most-recent-version)
    - [Pull updates from fork's upstream](#pull-updates-from-forks-upstream)

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

### Clone Recursively

This is if a repo has submodules.

**NOTE:** this is how the [main website repo](https://github.com/GWC-UNCC/Girls-Who-Code-at-UNCC) should be cloned.

1. Launch your command palette
2. type clone, and select the `Git: Clone (Recursive)` options

   ![clone recursive](/pictures/hugo-specific/img00.png)
3. Then follow the [normal clone instruction](/00-setup/README.md#clone-locally).

If you have already cloned the repository without the recursive option, then  you need to run [this command](#pull-submodules-after-clone).

### Pull submodules after clone

```git
git submodule update --init --recursive 
```

If you were following how to clone the main website, then you can stop here.

The following is just for general reference.

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

### Pull updates from fork's upstream

If you want to get updates from the main website repo and you already forked it ( after there were changes ), then you should be able to get the updates from the main repo by running these commands.

```shell
# windows operating system:
git remote add upstream https://github.com/GWC-UNCC/Girls-Who-Code-at-UNCC.git ; git fetch upstream ; git pull upstream main ; git submodule update --init --recursive
# *nix (i.e. Mac's ) operating system:
git remote add upstream https://github.com/GWC-UNCC/Girls-Who-Code-at-UNCC.git && git fetch upstream && git pull upstream main && git submodule update --init --recursive
```
