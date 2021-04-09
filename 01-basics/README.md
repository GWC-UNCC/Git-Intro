# Basics

Now you should have everything configured and a copy of this repository pulled down locally to your machine.

- [Basics](#basics)
  - [Add a file](#add-a-file)
  - [Check on your file](#check-on-your-file)
  - [Commit your file](#commit-your-file)
  - [Check on your commited file](#check-on-your-commited-file)
  - [Extra resources](#extra-resources)

## Add a file

If you click on the add file icon in the file explorer section, on the left hand side, then you can add a file to the repository.

![add file](/pictures/basics/img00.png)

You can name it anything, but remember to give it an extention ( i.e. `.txt` for text files ). Then hit `Enter` when you finish naming it. This will open it as the file you are editing.

![name file](/pictures/basics/img01.png)

Once you add some text to the file, go to `File` ➡️ `Save` ( now just known as `save`)

![save file](/pictures/basics/img02.png)

## Check on your file

You should notice now that the file's name now looks green, there is no more ⚪ next to the name, and it has a `U` next to it's name.
As well as on the far left hand side there is now a 1 that has popped up.

![saved file](/pictures/basics/img03.png)

Click on the icon with a 1 on it, and this will bring you to the "Source Control" view.
Here you should see your file which you just created under a section called "Changes".
The `U` stands for untracked changes, so that means while you added your file to folder the repo is in, git isn't tracking your changes to it yet.

![changes view](/pictures/basics/img04.png)

## Commit your file

Now we are going to commit this file, so that git will track you changes ( also allowing other to access it, since git will hold on to it ).
Click on the `+` next to the `U` under the "Changes" section.

![commit file](/pictures/basics/img05.png)

You will now notice that your file has an `A` next to it now, and instead of under the changes section your file is under the "Staged Changes" section.
The `A` means that your changes are staged and you are adding something.

![staged file](/pictures/basics/img06.png)

Now you are going to add some text in the Message box right above the "Staged Changes" section.
This text will be tied to your changes as a commit message.
You want make this message as descriptive as possible, because this is your log for the different changes you have made to files ( your future self/teammates will thank you 😁 ).

![commit message](/pictures/basics/img07.png)

When you are done, hit `Ctrl`+`Enter`.
Then you will get an error pop-up.
Click on the "Open Git Log" button.

![commit message](/pictures/basics/img08.png)

Click on the "TERMINAL" menu from the bottom pop-up.

![commit message](/pictures/basics/img09.png)

Type the following in your terminal* ( substitute <> with your information ):

```shell
git config --global user.email "<your_email>"
git config --global user.name "<your Github username>"
```

\* - you can normally launch your terminal by going to the `Terminal` menu option up top and clicking the `New Terminal` option.

Now go back to your commit message, and when you press `Ctrl`+`Enter` now it should be successful.
There should be no more files under the changes section ( img 1 ), but there is a new change to be pushed to the remote repository ( img 2 ).

![no more files](/pictures/basics/img10.png)

![new changes to push](/pictures/basics/img11.png)

Launch your command palette, and type `push` and hit `Enter`.

![push changes](/pictures/basics/img12.png)

## Check on your commited file

If you go back to your web browser, and refresh the page. Your file that you created should be there 🥳
Now you should be ready to go to the next step of the [tutorial](/README.md#steps).

As a note, it is normally preferred to commit often, because you can always collapse ( or squash ) how many commits are made.
You can't undo/get back commits you haven't made though ( if you make a mistake or your computer dies ).
So, it is generally recommended to commit frequently and small, with descriptive messages.
Just don't let it get in the way of the fun using vscode 😅.

## Extra resources

- making your email address private inside of git(hub): <https://docs.github.com/articles/setting-your-email-in-git>
- <https://git-scm.com/docs/git-add>
