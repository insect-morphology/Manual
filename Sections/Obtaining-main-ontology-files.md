# Get the ontology files to work from your computer #

Each **editor** will need to **fork** the main repository, hosted at [insect-morphology](https://github.com/insect-morphology), so that they can have their own copy of the full ontology to work with. This is achieved by pressing `Fork` on the top right side of the screen:

![GitHubFork2](https://github.com/insect-morphology/Manual/blob/main/img/GitHubFork2.png)

Any changes made to files on this fork will **not** affect the main repository until a pull request has been submitted **and** accepted.

Then you need to **clone your fork** of the main repository, to your computer, so that you can edit the appropriate file directly in your computer using [Protégé](https://protege.stanford.edu/). This step will copy all the files from the GitHub repository to your computer.

**For command line users:**

`git clone https://github.com/your_GitHub_user_name/abbreviation_for_your_ontology`

In my case, to be able to edit the AISM, this would be:

`git clone https://github.com/JCGiron/aism`


**For GitHub Desktop:**

Go to `File`, `Clone Repository` and find your forked repository in the list of available repositories to clone. Then click on `Clone`.

![GitHubDTClone](https://github.com/insect-morphology/Manual/blob/main/img/GitHubDT-Clone2.png){:height="60%" width="60%"}


Now you can explore the ontology folder on your computer. You should be able to see the same exact file system that is on your forked repository on GitHub.

The only file to be edited is the `src/ontology/abbreviation_for_your_ontology-edit.owl` file, using [Protégé](https://protege.stanford.edu/).{:height="50%" width="50%"}

For instructions on how to use [Protégé](https://protege.stanford.edu/) to edit the AISM or AISM-based ontologies, go to: [Using Protégé](https://github.com/insect-morphology/Manual/blob/main/Sections/Using-Protege.md).
