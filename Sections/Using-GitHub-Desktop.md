## Using [GitHub Desktop](https://desktop.github.com/) to upload your ontology as a [GitHub](https://github.com/) repository 

These steps need only to be followed by the **order-specific ontology manager**, as this person should have the initial files created using the [Ontology Development Kit](https://github.com/INCATools/ontology-development-kit). At this point, the **order-specific ontology manager** should have a cloned "placeholder repository" from [insect-morphology](https://github.com/insect-morphology) (see instructions at https://github.com/insect-morphology/Manual/blob/main/Sections/Upload-initial-ontology-as-GitHub-repository.md). This will set up a repository to be used by collaborators. Instructions for order-specific ontology editors can be found here: ---.

Open [GitHub Desktop](https://desktop.github.com/) and log in with your [GitHub](https://github.com/) credentials.

There should be a `GitHub` folder in the `Documents` folder in your computer at this point. 

Find your forked repository in the list of repositories shown on the main screen, and click "clone your_GitHub_user_name/abbreviation_for_your_ontology". Alternatively, click on "File" on the top menu and choose "Clone Repository", which will open a new window.

Find your forked folder in the list, click on it and hit "Clone" at the bottom right corner.

![GitHub Desktop - Clone](https://github.com/insect-morphology/Manual/blob/main/img/GitHubDT-Clone.png)

A window will pop up asking how you plan to use this forked repository. Choose the first option: _To contribute to the parent project_. Then click "Continue".

![GitHub Desktop - What for?](https://github.com/insect-morphology/Manual/blob/main/img/GitHubDT-WhatFor.png)

The program will take a moment to bring the files to your computer to finish on a screen with your forked repository. Just to be safe, make sure you click Fetch origin at the top before moving on to the next step.

![GitHub Desktop - Cloned](https://github.com/insect-morphology/Manual/blob/main/img/GitHubDT-Cloned.png)

This will create an `abbreviation_for_your_ontology` folder within `Documents/GitHub/` containing only one `README.md` file, identical to what is in your forked repository on the [GitHub](https://github.com/) website.

Now, go back to your computer folders and copy ALL the files from your `Documents/Ontology/target/abbreviation_for_your_ontology` folder and paste them into the freshly cloned folder (i.e. `Documents/GitHub/abbreviation_for_your_ontology`), overwriting (replacing) the README.md file that was already there.

<p>
<sub>
<b>Note:</b> If before using GitHub desktop you tried using git commandd and the procedure didn't quite work, and you are giving GitHubDesktop a try, you might have a .git folder within Documents/GitHub/abbreviation_for_your_ontology. DO NOT copy this folder, as it will create problems involving new branches that we don't need. If this is your first attempt at uploading, just keep going.
</sub>
</p>

Go back to [GitHub Desktop](https://desktop.github.com/). It should now show you on the left panel the list of files that you just copied into the folder, which are marked with a plus sign in green. The only file looking different should be the `README.md` file, which appears with a yellow square, indicating that the content of this file has been edited and is different from the file that was originally there. This is okay.

![GitHub Desktop - Commit](https://github.com/insect-morphology/Manual/blob/main/img/GitHubDT-Commit.png)

Now we need to commit these changes. On the bottom left there is space for doing this:

In the Summary field enter: `initial commit`

In the description: `Newly ODK-created AISM-based ontology files including first release`

This will activate the blue "Commit to master" button at the bottom. Press it.

Now the main panel on the right will show you options, the first of which is shaded in blue to _"Push commits to the origin remote"_. Press the "Push origin" blue button on the right side of the screen.

![GitHub Desktop - Push](https://github.com/insect-morphology/Manual/blob/main/img/GitHubDT-Push.png)

The program will take a moment and you will see the top field on the right changing and showing processing progress. When it is done pushing (uploading) the files, the light blue block will disappear.

![GitHub Desktop - Pushed](https://github.com/insect-morphology/Manual/blob/main/img/GitHubDT-Pushed.png)


Now you can go to your web browser and refresh/reload your forked repository to see all the files copied there from your computer, with this message at the top:

![GitHub Branch Ahead](https://github.com/insect-morphology/Manual/blob/main/img/GitHubBranchEven.png)
