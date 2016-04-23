# Getting started with Open Source
Materials for "Getting started with Open Source" at [DevPulseCon](http://devpulsecon.squarespace.com/sessions/#OpenSource)

This repository contains information to help you get started with contributing to an open source project on GitHub.
As part of this session, you will contribute a small change to this project to familiarise yourself with a typical workflow for contributing to projects on GitHub.

## Prerequisites
* GitHub account
* [git](https://git-scm.com/) installed on your local machine

If you're new to git, you can learn the basics in your browser using [Try Git](http://try.github.io/).

## Making your first contribution

### Fork this repository
Click the "Fork" button at the top right of this page.
You should now have a copy of this repository available on your own account.
You can make changes and freely experiment knowing that you won't be affecting the upstream repository.

### Clone the forked repository to your local machine
This copies the entire repository, including all history, to your local machine.

`git clone https://github.com/<username>/open-source-intro.git`

### Create a branch for your changes
Choose a short but descriptive name for your branch.
This will help you identify it amongst other branches.

```
cd open-source-intro
git checkout -b add-<name>-to-attendees
```

This command creates a new branch and switches the working branch to the newly created one.

### Make your changes!
Open the file `attendees.json` in your editor of choice.
Add a JSON object to the `attendees` array in the following format:

```
{
"name": "<Your name>",
"username": "<Your github username>"
}
```

### Check your changes
You can check the status of the repository and see which files have been modified using the following command:

`git status`

You can check that your changes are as expected:

`git diff`

### Commit your changes
Before committing the changes, we need to "stage" them first.

`git add attendees.json`

Once we've staged all of our changes, we commit them:

`git commit -m "Add <Your Name> to attendees."`


	* If this is your first time using git on your local machine, you will be asked at this point to input your name and email address.
	This is necessary as git uses this information in the commit metadata and GitHub identifies your commits by email address.
	Ensure that you use the same email address for both your GitHub account and git configuration.

	```
	git config --global user.name "<Your Name>"
	git config --global user.email "<email address used on github account>"
	```

	Once you've added this information, run the `git commit` step from before.

You can now check the logs and see your commit

`git log`

### Push your changes
Pushing your changes will make them publicly available on your GitHub repository.

`git push --set-upstream origin <branch-name>`

### Create a Pull Request
Once you've pushed all the changes you want to make, it's time to create a pull request to contribute the changes back upstream.

To create a pull request, go to the branches section on your GitHub repository.
Within this page, you should see your branch listed, and to the right of it, a button which says "New Pull Request".
Click this button.
The "Open a pull request" page allows you to write a title and comment for your pull request and allows you to compare your branch against the target branch in the upstream repository.
Once you're happy with the description, click "Create pull request".

### Wait for code review
Once you've created your PR, the project maintainers will review your change and decide whether it should be merged.
If changes are suggested, you can continue to make changes on your original branch and the pull request will be updated accordingly.

If the project maintainers are satisfied with your changes, they may merge your pull request.
Congratulations! You will have made a contribution to an open source project!
