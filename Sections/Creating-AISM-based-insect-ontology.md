# Creating an AISM based insect ontology using the Ontology Development Kit (ODK)

These steps need only to be followed by the **order-specific ontology manager**, as this will create the initial files to be used by collaborators. Instructions for order-specific ontology _editors_ can be found here: 

The first thing you need to do is to install the [Ontology Development Kit - ODK](https://github.com/INCATools/ontology-development-kit). We present here a modified version of the instructions provided at https://github.com/INCATools/ontology-development-kit.

Follow the steps carefully. This will create a file system in your computer with all the necessary elements to create and run your ontology, ready to be uploaded to [GitHub](https://github.com/), in a semi-automated way. This process might require some preparation and troubleshooting, especially if you are installing the [ODK](https://github.com/INCATools/ontology-development-kit) on a Windows machine (as it will need several additional background programs including linux), and if you are not experienced with and/or set up for working with [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) and [GitHub](https://github.com/) from your computer.

1. Create a folder in your computer to save all the necessary files to create your ontology. For these instructions we will refer to this folder as `Documents/Ontology`, which is a folder called Ontology within the Documents folder in the computer.

2. **Download and install [Docker](https://www.docker.com/get-started)**. (Mac users: minimum requirement is 10.13.2; make sure that Docker gets all the permissions needed in High Sierra and up).

3. Tell Docker to download and organize all the elements of the ODK. First, you will need to download the appropriate `seed-via-docker` script to your `Documents/Ontology` folder as a seed-via-docker.sh or .bat file:

**For Mac:** go to https://raw.githubusercontent.com/INCATools/ontology-development-kit/master/seed-via-docker.sh. Right click on the page, select "save as", and save the file in the your `Documents/Ontology` folder, without changing the file `.sh` extension.

**For Windows:** go to
https://raw.githubusercontent.com/INCATools/ontology-development-kit/master/seed-via-docker.bat. Right click on the page, select "save as", and save the file in your `Documents/Ontology` folder. Make sure that the file keeps only its `.bat` extension, by selecting "all files" as opposed to "Text document" in the "Save as type" field. If necessary, make sure to delete the extra `.txt` extension that Windows might have added.

Then, go to the command line and run the following command:

`docker pull obolibrary/odkfull`

This will install all the components required to use the [ODK](https://github.com/INCATools/ontology-development-kit). This may take a few minutes. You will see a list of files beeing completed over time, but no new files will appear in your `Documents/Ontology` folder.

4. **Create an `insect_order.yaml` file** in the `Documents/Ontology` folder (the same folder where you saved the `seed-via-docker` file). To do this, copy and paste the text below into a new text file in the text editor.

```
id: abbreviation_for_your_ontology 
title: full name of your ontology 
github_org: your_GitHub_user_name 
repo: name_of_repository
import_group:
  products:
    - id: aism
      mirror_from: https://raw.githubusercontent.com/insect-morphology/aism/master/aism.owl
```

DO NOT change any spacing at the beginning of lines in this text as it can produce errors running the commands.

In the text, edit the information according to your ontology. Make sure `your_GitHub_user_name` coincides with the user name for both the [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) settings in your computer and the [GitHub](https://github.com/) profile where you will be uploading your repository. The `name_of_repository` must coincide with the name of the "placeholder repository" that was created at [insect-morphology](https://github.com/insect-morphology).

For example:

```
id: colao
title: Coleoptera Anatomy Ontology
github_org: jcgiron
repo: colao
import_group:
  products:
      - id: aism
        mirror_from: https://raw.githubusercontent.com/insect-morphology/aism/master/aism.owl
```

Save this file as `insect_order.yaml` (not `.txt` by accident [in Windows make sure that the option "All files" is selected instead of text file, and that there is no `.txt` in the file name; e.g., colao.yaml) in the same folder where you saved your `seed-via-docker` file (i.e. your `Documents/Ontology` folder).

Go back to the command line and run the `seed-via-docker` command (see below). Make sure that before you run this command, your command line is set to the folder where the `seed-via-docker` file is located, using the `cd` command in the command line (i.e. `cd Documents/Ontology`).

**For Mac:** 

`sh seed-via-docker.sh -C insect_order.yaml`

**For Windows:**

`./seed-via-docker.bat -C insect_order.yaml`

The `seed-via-docker` command will execute and you will see a quickly growing list of printed commands and results on the screen. It will get to a point where this printing stops for a minute and then resume to show you a block of text starting with:

```
####
NEXT STEPS
```

Do not follow those steps just yet (those are the steps to upload your ontology files to [GitHub](https://github.com/)), but keep going with the steps below. You will do this upload later when the initial files are updated to incorporate the **_simplified version of the AISM_**. The instructions for uploading will be given then.

If the few last lines in your command line start with `Exception: Failed…` it means that something went wrong and you need to repeat step 4, including checking your `.yaml` file for errors. In case you are having trouble with your `insect_order.yaml` file, there is a [sample file here](https://github.com/insect-morphology/Manual/blob/main/Sections/insect_order.yaml) that you can download, edit, save, and use.

When this processs fails, it might create a new folder with incomplete files.

To make sure that the files are complete, there should be a folder called `target` within your `Documents/Ontology` folder. Within `target` there should be one folder named `abbreviation_for_your_ontology` containing three folders (`imports`, `reports` and `src`) and a few additional files starting with the same `abbreviation_for_your_ontology` name with different extensions (i.e. `.owl`, `.obo`). Within `src` there should be five folders: `metadata`, `ontology`, `patterns`, `scripts`, and `sparql`. Within `ontology`, there should be three folders: `imports`, `mirror`, and `reports`, plus several additional files, including an `abbreviation_for_your_ontology-odk.yaml` file.

If it did not work or there are mistakes in the initial `.yaml` file, do not worry, you can delete the newly created folders (if there are any) and start over with step 3 as many times as necessary until it works properly and has all the required files.


## Setup AISM based ontology imports

In order to use the **_simplified version of the AISM_** (refer to the [Background](https://github.com/insect-morphology/Manual-for-AISM-based-insect-anatomy-ontologies) section) you will need to edit one of the files that were just created using the [ODK](https://github.com/INCATools/ontology-development-kit).

In the newly created file system, there will be a folder called `target`. Inside that folder there should be a folder with the name of your ontology (i.e., `abbreviation_for_your_ontology`). Open that one and you should find a folder called `src`, then go to the folder `ontology` within `src`, find the file  `abbreviation_for_your_ontology.Makefile`, and open it in the text editor.

Copy the text below and paste it below the text that is already in the file. DO NOT change any spacing in this text, especially at the beginning of lines, as it can interfere with running the commands and make the script not work properly.

```
AISM_BASE="https://raw.githubusercontent.com/insect-morphology/aism/master/aism-base.owl"
mirror/aism-base.owl:
	if [ $(MIR) = true ] && [ $(IMP) = true ]; then $(ROBOT) convert -I "$(AISM_BASE)" -o $@.tmp.owl && mv $@.tmp.owl $@; fi
.PRECIOUS: mirror/aism-base.owl
tmp/seed_aism_base.txt: mirror/aism-base.owl
	@if [ $(IMP) = true ]; then $(ROBOT) query -i $< -q ../sparql/terms.sparql $@; fi
imports/aism_import.owl: mirror/aism.owl tmp/seed_aism_base.txt
	@if [ $(IMP) = true ]; then $(ROBOT) remove -i $< -T tmp/seed_aism_base.txt --select complement --select "classes individuals" \
		remove --exclude-terms keep_ann.txt --select annotation-properties \
		remove --exclude-terms keep_obp.txt --select object-properties \
		annotate --ontology-iri $(ONTBASE)/$@ --version-iri $(ONTBASE)/releases/$(TODAY)/$@ --output $@.tmp.owl && mv $@.tmp.owl $@; fi
.PRECIOUS: aism_import.owl
```

Save the file (i.e. go to file, then save - without changing the name of the file).

Now, you will also need two files containing the properties that we are keeping to have a working and decluttered AISM version:
- [Annotation properties](https://raw.githubusercontent.com/insect-morphology/Manual/main/Sections/keep_ann.txt)
- [Object properties](https://raw.githubusercontent.com/insect-morphology/Manual/main/Sections/keep_obp.txt)

For each file: Go to the link, right-click, save as .txt file in your `abbreviation_for_your_ontology\src\ontology\` folder as keep_ann.txt and keep_obp.txt.

Now, go back to the command line and go all the way to this ontology folder (i.e. `cd \target\abbreviation_for_your_ontology\src\ontology\`). Then update the files using the following command:

**For Mac:**

`sh run.sh make update_repo`

**For Windows:**

`./run.bat make update_repo`
 
You should get this message: `Update successfully completed` right when the command line is done processing. If not, there must be a problem with the `Makefile` you just edited. Please check the previous step carefully.

Then make the imports using the following command:

**For Mac:**

`sh run.sh make all_imports`

**For Windows:**

`./run.bat make all_imports`

And lastly, refresh the files:

**For Mac:**

`sh run.sh make refresh-aism`

**For Windows:**

`./run.bat make refresh-aism`

To check if everything went well, open the file `abbreviation_for_your_ontology-edit.owl` in [Protégé](https://protege.stanford.edu/). The main screen should look similar to the image below:

![Protégé Home Screen](https://github.com/insect-morphology/Manual/blob/main/img/ProtegeHome.png)


At this point, it is recommended that you edit the main annotations of your newly created ontology, by pressing the circle icon on the right side of the main panel:
1. Adjust the title if needed.
2. Add a brief description of the contents of your ontology.
3. Add a license. We recommend https://creativecommons.org/licenses/by/4.0/.
4. You can add contributors by pressing the plus sign at the top of the main panel and scrolling to find the annotation "contributor". The recommendation is to include name, a short version of the name, and the full ORCID link for the person (e.g. Jennifer C. Girón (jgiron) https://orcid.org/0000-0002-0851-6883).

Then save the ontlogy file and run your first release, which is the last step using the [ODK](https://github.com/INCATools/ontology-development-kit) for now, make release files, before uploading files to [GitHub](https://github.com/):

**For Mac:**
`sh run.sh make prepare_release`

**For Windows:**
`./run.bat make prepare_release`

This will run the [ODK](https://github.com/INCATools/ontology-development-kit) to make some verifications and create the first version of the ontology ready to be used and edited by collaborators. This will give you a report of errors coming from your imports ([AISM](https://github.com/insect-morphology/aism)). Do not worry about this at this point.

Also, take a look at the instructions on the `README-editors.md` file within your `src/ontology/` folder, by opening the file in the text editor.

After your files have been created, edited and released, you are ready to [upload this first version of the ontology to GitHub](https://github.com/insect-morphology/Manual/blob/main/Sections/Upload-initial-ontology-as-GitHub-repository.md).
