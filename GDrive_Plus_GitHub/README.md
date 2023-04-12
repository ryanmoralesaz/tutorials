# Using Google Drive Desktop App and Github

1. Make sure you have Google Drive App for Desktop installed

2. Create a new project folder in your Google Drive  
   ![New Folder](new_folder.png 'Creating a new folder in gdrive')

3. | Option A                                                                                  | Option B                                          |
   | ----------------------------------------------------------------------------------------- | ------------------------------------------------- |
   | `CD` into the project from terminal On windows use: `CD /d "G:My\ Drive\path_to_project"` | Click on the folder path in finder and type `CMD` |

4. Inside the project folder run:

   > `git init`

5. `git branch -m master main`

   > to rename and checkout the default branch

6. `echo "# New Project" >> README.md`

   > to add a readme in the root of the folder with a title

7. `git add .`

   > to add the new readme to be tracked by git

8. `git commit -m "first commit added readme"`

   > to make the first commit

9. Go to your github page in the browser

10. Create a new repository by clicking the green button "NEW"
    ![New Repo](new_github_repo.png 'Creating a new repository in github')

11. Name the repository and provide a description
    > - You can make it public or private
    > - Do NOT check "add a readme"
    > - Do NOT initialize a .gitignore file
    > - You can select a copyright option if you like

![Name Repo](name_repository.png 'Creating a new repository in github')

12. Click green "create repository button"

13. Copy the url of the repository

    > You may use SSH or HTTP depending on your needs.

14. Open your new project in VS Code and make sure to open an integrated terminal in that folder location

![Open VS Code](VS_Code.png 'Open your project in vs code with a terminal')

15. !IMPORTANT!

    > Do NOT add any other folders to this VS Code instance. Git is currently tracking this folder and it can confuse git adding other folders that may be already tracked.

16. `git status`

    > to check that your folder is initialized with git and ensure your first commit has been made

17. `git branch teacher_branch`

    > to create a new git branch where you can make drafts

18. `git checkout teacher_branch`

    > to switch to the teacher drafting branch

19. Ensure at the bottom bar of VS Code that you are on the "teacher_branch"

20. Add a new file called "test.txt" in the root of the project (the same location as the readme) and write "testing teacher_branch"

21. Save the file and run `git add .`

22. `git commit -m "added test file"`

23. `git checkout main`

    > to switch back to the main branch. Your test file should not be visible. Your test file still exists on the teacher_branch.

24. To see your files on the teacher_branch run  
    `git ls-tree --name-only teacher_branch`

25. Add your github repository as an origin to push to  
    `git remote add origin /Github.com/URL/Path_Name`

    > As an example if using SSH it would look like  
    > `git remote add origin git@github.com:WestMecRyan/New_Project.git`

26. Run `git remote -v`

    > To confirm that the origin has been added

27. `git status`

    > to confirm that your working tree is clean, there are no commits: you are ready to push

28. `git push -u origin main`

    > will push your local repo to github. the -u flag sets the origin as the 'upstream' for your main branch so you will only need `git push` for future pushes.

29. If you receive an error message about your access permissions you will need further assistance
    > - you may have a problem with your SSH key access
    > - you may need to use github desktop app to access your github repos using HTTP
30. If successful -> Go to your github repo in the browser to ensure that your files have been pushed and are live.

31. In VS Code `git checkout teacher_branch test.txt`

    > you have now merged the test file from the teacher branch into your main branch.
    >
    > - you can `git add .`
    > - then `git commit -m "added test.txt"`
    > - then `git push`
    >   to push your test file to github  
    >   OR
    >
    > * you can delete the test.txt with  
    >   `rm test.txt`
    >
    > - then `git add .`
    > - then `git commit -m "removed test"`

    32. If you `git checkout teacher_branch `
        > you should see that the test.txt file still exists on the teacher_branch

## Conclusion

Using this method you can create documents in the teacher_branch before merging them to the main branch that you can push to be public

> - To test how the students would retrieve the files

1. `CD` into your projects folder
2. `git clone git\Repo\URL.git`
   > - this will create a new folder in your projects folder named after the repo and download all of the public github documents from the github repo into the new folder
