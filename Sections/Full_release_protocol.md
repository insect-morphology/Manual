# Full release protocol #

The  **ontology manager** will need to generate, upload, and push **release files** whenever there are changes in the ontology. Once the files are in the main repository, there are additional steps in order to create a working version of the ntology that can be used by others.

**1. Make sure that your [ODK](https://github.com/INCATools/ontology-development-kit) is up to date:**
Using the command line, go all the way to your ontology folder (i.e. `\abbreviation_for_your_ontology\src\ontology\`)
and run: 
`docker pull obolibrary/odkfull`

When it is done, run twice: 

**For Mac:**
`sh run.sh make update_repo`

**For Windows:**
`./run.sh make update_repo`

**2. Prepare your new release files:** Depending on your imports, this might take a while.

**For Mac:**
`sh run.sh make IMP_LARGE=false prepare_release`

**For Windows:**
`./run.sh make IMP_LARGE=false prepare_release`
