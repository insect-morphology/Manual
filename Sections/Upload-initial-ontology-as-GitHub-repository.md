# Uploading the ontology to the GitHub repository

These steps need only to be followed by the **order-specific ontology manager**, as this person should have the initial files created using the [Ontology Development Kit](https://github.com/INCATools/ontology-development-kit). This will set up a repository to be used by collaborators. Instructions for order-specific ontology editors can be found here:


### Setting [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

For all steps involving interactions with [GitHub](https://github.com/), your installation of [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) must be set to work with your GitHub user. For this you need to add your GitHub username and the email you use with that account to git.

Go to the command line

To add your user name type:
`git config --global user.name 'your_GitHub_user_name'`

To add your user email type:
`git config --global user.email 'email_address_used@this_account'`

For example:

`git config --global user.name 'JCGiron'`

`git config --global user.email 'entiminae@gmail.com'`


### Fork the "placeholder repository" hosted at [insect-morphology](https://github.com/insect-morphology)

Go to `https://github.com/insect-morphology/abbreviation_for_your_ontology` and press the "Fork" button on the top right corner within the repository. This creates a copy of this repository into your user's profile, so that the newly created ontology files can be uploaded there.

![GitHub Fork](https://github.com/insect-morphology/Manual/blob/main/img/GitHubFork.png)

Then go back to the repositories in your profile. There should be a forked repository called `your_GitHub_user_name/abbreviation_for_your_ontology`, in my case `https://github.com/JCGiron/colao`. You should see something like this near the top left when you access the repository:

![GitHub Branch](https://github.com/insect-morphology/Manual/blob/main/img/GitHubBranch.png)

From here, you can either:

- [Use git commands in the command line](https://github.com/insect-morphology/Manual/blob/main/Sections/Using-git-commands.md)

or

- [Use GitHub Desktop](https://github.com/insect-morphology/Manual/blob/main/Sections/Using-GitHub-Desktop.md)

After you upload your ontology files into your forked repository, you can go ahead and [submit a pull request](https://github.com/insect-morphology/Manual/blob/main/Sections/Submit-pull-request.md) so that [insect-morphology](https://github.com/insect-morphology) admins can review and pull your files into the original repository.
