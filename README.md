1. `git init` --> Powers your folder to be managed by Git, and initialises a new empty repository. It also creates a .git folder that has also the relevant logic to manage different versions of your project.

2. `Working Area` --> There can be a bunch of files that are not currently handled by git. It means that changes done or to be done in those files are not maanged by git yet. A file which is in working area is considered to be not in the staging area. When we do `git status` and we see a bunch of 'untracked files' then these are actually called to be in the working area.

3. `Staging area` --> What all files are going to be a part of the next version that we will create. This staging area is the place where git knows what changes will be done from the last version to the next version.

4. `Repository area`--> This area actually contains the details of all the previous registered versions. And the files in this area, git already manages them and knows their version history.

5. `git add <file>` --> Moves file from working area to staging area

6. `git rm --cached <file> ` --> Moves file back from staging area to working area

7. `commit` --> git commit is a particular version of the project. It captures a snapshot of the project's staged changes and creates a version out of it.

8. `git commit` --> registers staging changes to a commit 

9. `git log` --> lists down all the commits of the repository. If you want to exit out of git log, press 'q'.

10. `git restore <file> ` --> two different usecases

Unstaged Changes: If you have made changes to a file in your working directory but have not yet staged those changes, you can use git restore <filename> to discard those changes and revert the file to the state it was in the last committed version.

Example:

git restore myfile.txt

Staged Changes: If you have already staged changes (using git add) but want to unstage them, it cannot be simply done with git restore <filename>. We need to use git restore --staged <filename>.

Example:

git restore --staged myfile.txt

Doing this will move the changes from staging area to working area. Now I can discard the changes from the working area by using `git restore <filename>` as before.

An easy real life analogy to understand about the working area, staging area and the repository :

Think of a mathematics examination. We have an answer sheet and a rough sheet. Now in order to solve the first question, we do some rough work on the rough sheet. That is the working area. Any changes or work that we do in this rough area may/may not work.

What we need to submit to the teacher is the answer sheet, so we copy the solution from the rough sheet to the answer sheet. The answer sheet is the working area.

After the exam gets over, the invigilators click a photograph of the answer sheet for their future records. This is what the repository is.

11. `git diff <commit-id1> <commit-id2>` : Considering commit-id1 to be the previous commit and commit-id2 to be the further commit, it tells the difference between the two commits in terms of additions and deletions of code.