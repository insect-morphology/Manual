## Using git commands to upload your ontology as a GitHub repository 

These steps need only to be followed by the **order-specific ontology manager**, as this person should have the initial files created using the [Ontology Development Kit](https://github.com/INCATools/ontology-development-kit). At this point, the **order-specific ontology manager** should have a cloned "placeholder repository" from [insect-morphology](https://github.com/insect-morphology) (see [Uploading the ontology to the GitHub repository](https://github.com/insect-morphology/Manual/blob/main/Sections/Upload-initial-ontology-as-GitHub-repository.md)). This will set up a repository to be used by collaborators. Instructions for order-specific ontology editors can be found here: ---.


There should be a `GitHub` folder in your computer at this point. If there is none, go ahead and create a folder called `GitHub` in the `Documents` folder in your computer. In the command line, cd into your `GitHub` folder (i.e. `cd Documents/GitHub`) and `clone` the repository that you forked from [insect-morphology](https://github.com/insect-morphology) using its web address:

`git clone https://github.com/your_GitHub_user_name/abbreviation_for_your_ontology`

In my case: `git clone https://github.com/JCGiron/colao`

This command will create an `abbreviation_for_your_ontology` folder within `Documents/GitHub/` containing only one `README.md` file, identical to what is in your forked repository on the GitHub website.

Now, go back to your computer folders and copy ALL the files from your `Documents/Ontology/target/abbreviation_for_your_ontology` folder and paste them into the freshly cloned folder (i.e. `Documents/GitHub/abbreviation_for_your_ontology`), overwriting (replacing) the `README.md` file that was already there.

Go back to the command line and `cd` into the `Documents/GitHub/abbreviation_for_your_ontology` folder and type:

`git status`

This should show you the list of files that you just copied into the folder in red, which indicates that these files are only in your computer, but not in the GitHub repository.

Next, we need to add these files to the "staging area" to be able to upload them to GitHub by entering:

`git add .`

This will stage all the new files, so that if you enter `git status` again, the same files that were in red will appear in green this time, which means that they are ready to be committed and pushed to GitHub. Then enter:

`git commit -m "initial ontology files including first release"`

And lastly, enter:

`git push`

Now you can go to your web browser and refresh/reload your forked repository to see all the files copied there from your computer, with this message at the top:

![GitHub Branch Ahead](https://github.com/insect-morphology/Manual/blob/main/img/GitHubBranchEven.png)
