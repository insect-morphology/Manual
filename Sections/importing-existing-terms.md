## Importing terms from existing ontologies ##

Open your `ontology-edit.owl` file.

Find your term online and copy its IRI.

In the classes window in Protégé, click on `owl:Thing` and then press `add subclass`.


<img src="https://github.com/insect-morphology/Manual/blob/main/img/ProtegeAddClass.png" alt="ProtegeAddClass" width="60%"/>


Which opens a new window:


<img src="https://github.com/insect-morphology/Manual/blob/main/img/ProtegeImportClass.png" alt="ProtegeImportClass" width="60%"/>


Paste your link to the Name field and click OK


<img src="https://github.com/insect-morphology/Manual/blob/main/img/ProtegeImportClassIRI.png" alt="ProtegeImportClassIRI" width="60%"/>


The term will now be listed under `owl:Thing`. You don’t need to worry about annotations or placement of this new item in the ontology. Keep adding existing terms from other ontologies, as needed.

Save the file. Commit and push the changes to GitHub, and [submit a **pull request**]((https://github.com/insect-morphology/Manual/blob/main/Sections/Submit-pull-request.md)), making sure to mention that this commit contains **imported terms**.

### Ontology manager ##

In order to import the hierarchy and properties for these newly imported terms, the **ontology manager**, who has the full ODK installation must run the imports:

1. Review and accept changes incorporated in the pull request.
2. Fetch the new changes to your computer.
3. In the terminal, go to the `src/ontology` folder and run:

`./run.sh make all_imports`

This will incorporate all the imported terms. It might take a couple of minutes for the system to find and organize all the information.
