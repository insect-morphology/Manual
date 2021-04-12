# Editing the AISM and AISM-based ontologies using [Protégé](https://protege.stanford.edu/) #

Here we outline the steps to be able to add, edit and annotate an existing [AISM-based](https://github.com/insect-morphology/aism) ontology. Some instructions here are adopted from the [Gene Ontology protocols](https://go-protege-tutorial.readthedocs.io/en/latest/).

In order to perform the steps in this section you will need to:
1. Have [Protégé](https://protege.stanford.edu/) installed
2. Have a clone of your forked repository in your computer

-------------------

## Explore the ontology and its hierarchy ##

Open Protégé. Click on `File`, `Open…`, and find the `abbreviation_for_your_ontology-edit.owl` file (e.g., `GitHub/abbreviation_for_your_ontology/src/ontology/abbreviation_for_your_ontology-edit.owl`

In my computer, this is
`GitHub/aism/src/ontology/aism-edit.owl`


 by clicking the entities tab in the top left area:


<img src="https://github.com/insect-morphology/Manual/blob/main/img/ProtegeHome.png" alt="ProtegeHome" width="80%"/>


This will show you the main features that you will be working with:
- The **classes** window (left block, outlined in blue), where you can see the hierarchy
- The **annotations** window (top box on the right, outlined in green)
- **Description** window (bottom box on the right, outlined in pink)
- Annotation properties tab (top left, red arrow)
- **Object properties** tab (top left, yellow arrow)


<img src="https://github.com/insect-morphology/Manual/blob/main/img/ProtegeMain.png" alt="ProtegeMain" width="60%"/>


Next, [setup Protégé to auto generate IRI-s](https://github.com/insect-morphology/Manual/blob/main/Sections/Setup-Protege.md).