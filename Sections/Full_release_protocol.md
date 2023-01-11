# Full release protocol #

The  **ontology manager** will need to generate, upload, and push **release files** whenever there are changes in the ontology. Once the files are in the main repository, there are additional steps in order to create a working version of the ntology that can be used by others.

**1. Make sure that your [ODK](https://github.com/INCATools/ontology-development-kit) is up to date:**
Using the command line, go all the way to your ontology folder (i.e. `\abbreviation_for_your_ontology\src\ontology\`)
and run: 'docker pull obolibrary/odkfull' when it is done, run twice 'sh run.sh make update_repo'.
