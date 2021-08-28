# Initial Setup

This will be the intial steps we are going to do in order to setup for this workshop.

- [Initial Setup](#initial-setup)
  - [Install Git](#install-git)
    - [Windows](#windows)
    - [OSX](#osx)
  - [GitHub auth to VSCode](#github-auth-to-vscode)
  - [Fork Repository](#fork-repository)
  - [Clone locally](#clone-locally)

## Install Git

### Windows

- TEsting
  - Press Shift + Right click the windows logo ( bottom left corner )
  - Click on the “Windows PowerShell (Admin)” option ![admin powershell](/pictures/intro/img00.png)
  - Click “Yes” at the administrative prompt
- Using chocolatey install git:

   ```powershell
   choco install git -confirm
   ```

### OSX

You either have git installed or it should be relatively easy to install git.
According to [this](https://apple.stackexchange.com/questions/304100/is-git-pre-installed-on-macos-sierra#304101) article you should to do this to install it:

- Launch a terminal.
- Then type `git`
- Hit `Enter`
- If you have it, then it should output some help information, and if you don't then it should prompt you to install it.

## GitHub auth to VSCode

We will be authenticating VSCode to your github account. This will allow you to do most interactions inside of vscode, instead of trying to learn the commands for the git CLI.

1. Open VSCode ( if you had vscode open before installing git, close and then re-open it )
2. Click on the `View` menu option in the top left
3. Then click on the `Command Palette...` option.*

   ![command palette](/pictures/intro/img01.png)

4. type `clone` in the box and hit `Enter`

   ![clone](/pictures/intro/img02.png)

5. Ensure you have the `Clone from GitHub` option, and click on it

   ![clone from GH](/pictures/intro/img03.png)

6. You should get a popup asking if you want to allow the extension GitHub to sign in to GitHub, click `Allow`

   ![allow extension](/pictures/intro/img04.png)

7. Click `Continue`

   ![start GH auth](/pictures/intro/img05.png)

8. Login to github

   ![GH Login](/pictures/intro/img06.png)

9. Click `Authorize github`

   ![Authorize github](/pictures/intro/img07.png)

10. Click the `Open` button.
   ![web browser popup](/pictures/intro/img08.png)

11. Click `Open`

   ![vscode popup](/pictures/intro/img09.png)

\* - **NOTE**: to the right of the option you will see a set of keys you can press on your keyboard to launch the command palette without clicking.
Also, this will now be referenced as "command palette" for the rest of the instructions.

Now don't do anything else with vscode yet, but continue to the next section.

## Fork Repository

We aren't going to go into what we are doing just yet, but for now go to your browser and click on the fork button for this repository.

![fork button](/pictures/intro/img10.png)

Wait for it to finish.

![fork button](/pictures/intro/img11.png)

Then you should be good to continue.

## Clone locally

- In your browser click on the `Code` button, and then the clipboard icon to copy the https url into your clipboard.

   ![clone from GH](/pictures/intro/img12.png)
- Go back to vscode, and launch your command palette.
- Then type `clone`, hit `Enter`, and click `Clone from GitHub`

   ![clone from GH](/pictures/intro/img03.png)

   - **NOTE:** the [main website repo](https://github.com/GWC-UNCC/Girls-Who-Code-at-UNCC) is cloned a bit diferently. see [here](/03-hugo_specific/README.md#clone-recursively)
- Paste the url you had copied before, and hit `Enter`

   ![paste url to command palette](/pictures/intro/img13.png)
- Choose a location to save this source code. ( I recommend keeping all your source code in one folder ( it can get quite unruly if you don't 😅 ))

   ![choose location](/pictures/intro/img14.png)

- In the bottom right hand corner of your vscode window there should be a pop-up saying that it is cloning the repository.
  When it finishes, you should get another pop-up like the one below. Click the `Open` button.

   ![open](/pictures/intro/img15.png)

- In the bottom left hand corner there is a bi-directional arrow ( picture below ), click on that.

   ![click bi-directional arrows](/pictures/intro/img16.png)
- When the pop-up shows, click `OK`

   ![accept push & pull](/pictures/intro/img17.png)
- Then, after a few seconds, in the bottom right corner there should be another pop up which asks about periodic fetching. Click `Yes` for that.

   ![accept push & pull](/pictures/intro/img18.png)

Now you should be ready to go to the next step of the [tutorial](/README.md#steps). 😁🎉
