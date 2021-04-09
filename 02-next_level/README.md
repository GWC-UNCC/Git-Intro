# Next Level

These are the next level steps you should learn to further expand on how to collaborate with others.

- [Next Level](#next-level)
  - [Log view](#log-view)
  - [Adding multiple changes](#adding-multiple-changes)
  - [Undo](#undo)
  - [Branching](#branching)
    - [Branching for issues](#branching-for-issues)
  - [Pull Requests](#pull-requests)
  - [Merging](#merging)

## Log view

Go back to vscode, and on the Source Control view at the bottom ( if you installed GitLens ), then you should see a few more menu options ( commits, file history, etc... ).
These are menus to help enrich your view of git from vscode.
For instance, if you click on the "FILE HISTORY" option you should see all modifications to the current file you had open ( which should be the file you just pushed )

![file history](/pictures/next-level/img00.png)

Your commit message should show there, and this is extremely helpful if you are trying to understand changes to a file.

## Adding multiple changes

Add a few files to your local repo version. ( remember you need to go back to the file explorer view to add them )

Now go back to your source control view.
If you look to the right of the "Changes" section, there is a `+` option.
This will bulk add all the changes made to the repository instead of you having to add the changes individually.

![bulk add](/pictures/next-level/img01.png)

Click on the bulk add to add all the files to the "Staged Changes" section.

## Undo

Now if you made changes that didn't work out, and you want to undo them.
You can do that :slightly_smiling_face:.
First let's add some text to the original document we created, look at your document, then remove a word or two, and save it again.

There are a few things that happened when we did that:

1. since we added text to the document initially our document was showing green as though we added to the line.

    ![initial change](/pictures/next-level/img02.png)

2. When we removed the text, the lines changed to blue ( this means we both added ( normally green ) and removed ( normally red ) things, because it is blending the red and green together ).

    ![combined changes](/pictures/next-level/img03.png)

3. If you look at the changes window ( above ) you will now see that there is a `M` next to the original text document.
   This is because our changes are now a modification instead of adding.

If you click on the modified file ( see above ) under the source control window while it shows the `M`, then you will see the changes you made inline to the file.
Left is always the original state of the file, and right is the current state of the modified file.
Deletions will always show on the left ( original state ), and additions are on the right ( current state ).
( You can only show deletions in the original state of the document, and additions will always be reflected in the current state. )

![combined inline changes](/pictures/next-level/img04.png)

Now if you want to undo those changes simply click the undo arrow ( for that file ), which is next to the add button for the file.

![undo button](/pictures/next-level/img05.png)

Then click "Discard Changes"

## Branching

Branching allows you to experiment with some code, while keeping your main/master branch clean and in a working state.
It is good to establish naming conventions for branches like `feat/<feature_name>/<issue_number>` ( i.e. `feat/adding_chat_bot/1` ) or `bug/<bug_name>/<issue_number>` ( i.e. `bug/fixing_text/2` ).
This helps delineate what the branches are for even before looking at the code.

So, you should still have your staged changes of the bulk added files ( if not just add a few more to the staged changes ).

1. Launch your command palette
2. Type branch, and make sure you select `Git: Create Branch...`

   ![branching option](/pictures/next-level/img06.png)

3. Name the branch: `feat/extra_files/1` ( no spaces allowed ) & hit `Enter`

   ![branch name](/pictures/next-level/img07.png)

4. Now you should see the branch's name in the bottom left corner

   ![branch name](/pictures/next-level/img08.png)

5. So, if you got to commit these files now, it will be to this branch
6. Then push the changes, and you will get a pop-up. Hit "OK"

   ![branch name](/pictures/next-level/img09.png)

7. Go back to your browser and refresh the page. You should see a new yellow box saying you had a recent push to your branch you just created. ( don't compare and pull yet, we will do that soon :slightly_smiling_face: )

   ![branch name](/pictures/next-level/img10.png)

### Branching for issues

**NOTE:** feat ( short for feature ) is adding an enhancment to the repository ( repo ), while bug is trying to fix something that was/has broken in the repo.

When someone submits an issue for a feature or bug, it is automatically  assigned an issue number.
You then can create a feature or bug branch from the main branch with `feat/<feature_name>/<issue_number>` or `bug/<bug_name>/<issue_number>`.
The issue number for that branch should match the submitted issue it was created to address.
Each feature/bug name should have one issue number.
That submitted issue is where you should have detailed information as to what you are trying to accomplish, and that issue will also be tied to a pull request.
We will look at issues more in depth another time, but for now let's go over a pull request.

## Pull Requests

Pull requests allow your teammates time to look through your code and make sure you following conventions, as well as make helpful suggestions for how to improve things ( more on this [here](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests) ).

They also allows you to easily merge your branches back into your main branch after you have sucessfully experimented with the code.
Normally you would have detailed information about what you are trying to accomplish in an issue, which is used to clarify/identify wanted features, bugs, and future plans ( more info about issues [here](https://guides.github.com/features/issues/)).

Looking at the previous picture, click on the "Compare & pull request" button.

Make sure the pull request is going against your main repository and not the GWC-UNCC original repo.
For now just click "Create pull request", but normally you would want to tie your issue to this PR by including some [keywords](https://docs.github.com/en/github/managing-your-work-on-github/linking-a-pull-request-to-an-issue)

![branch name](/pictures/next-level/img11.png)

This will create a pull request ( PR ), and shows you what changes will be made to the repository if this PR is successfully created.

## Merging

For now we are just going to click "Merge pull request", and "Confirm merge".
Normally you would want to get approval from other people to ensure everything looks good, but this is a tutorial 🙂

Everything should have sucessfully merged, congrats! 😁
Now you should be ready to go to the next step of the [tutorial](/README.md#steps).
