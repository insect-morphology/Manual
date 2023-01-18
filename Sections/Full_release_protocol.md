# Full release protocol #

The  **ontology manager** will need to generate, upload, and push **release files** whenever there are changes in the ontology. Once the files are in the main repository, there are additional steps in order to create a working version of the ntology that can be used by others.

## **1. Make sure that your [ODK](https://github.com/INCATools/ontology-development-kit) is up to date:** ##
Using the command line, go all the way to your ontology folder (i.e. `\abbreviation_for_your_ontology\src\ontology\`)
and run: 
`docker pull obolibrary/odkfull`

When it is done, run twice: 

**For Mac:**
`sh run.sh make update_repo`

**For Windows:**
`./run.sh make update_repo`

## **2. Prepare your new release files:** ## 
Depending on your imports, this might take a while.

**For Mac:**
`sh run.sh make IMP_LARGE=false prepare_release`

**For Windows:**
`./run.sh make IMP_LARGE=false prepare_release`

If your release is successful, you will see this message at the end of the process:

*"Release files are now in ../.. - now you should commit, push and make a release on your git hosting site such as GitHub or GitLab"*

## **3. Push all the new files to your repository** ##

`cd` into the `Documents/GitHub/abbreviation_for_your_ontology` folder and type:

`git status`

This should show you the list of files that changed in the main repository folder in red, which indicates that these files are only in your computer, but not in the GitHub repository.

Next, we need to add these files to the "staging area" to be able to upload them to GitHub by entering:

`git add .`

This will stage all the new files, so that if you enter `git status` again, the same files that were in red will appear in green this time, which means that they are ready to be committed and pushed to GitHub. Then enter:

`git commit -m "new changes and new release release"`

And lastly, enter:

`git push`

Now you can go to your web browser and refresh/reload your forked repository to see all the files copied there from your computer, with this message at the top:

![GitHub Branch Ahead](https://github.com/insect-morphology/Manual/blob/main/img/GitHubBranchEven.png)

Go ahead and [submit a pull request](https://github.com/insect-morphology/Manual/blob/main/Sections/Submit-pull-request.md) so that [insect-morphology](https://github.com/insect-morphology) admins can review and pull your files into the original repository.

# **For main repository admins:** #

Once the pull request has been reviewed and merged go ahead and create a new release in the repository. 

The tag should be in the format: vYear-Month-Day (e.g., v2022-10-08).

By creating a new release in the repository, the linked Zenodo repository will also be updated. Make sure that the new Zenodo version is also clean and complete. Don't forget to update the citation in the README file for your freshly released ontology.
