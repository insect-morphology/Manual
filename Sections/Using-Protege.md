# Editing the AISM and AISM-based ontologies using [Protégé](https://protege.stanford.edu/) #

Here we outline the steps to be able to add, edit and annotate an existing [AISM-based](https://github.com/insect-morphology/aism) ontology. Some instructions here are adopted from the [Gene Ontology protocols](https://go-protege-tutorial.readthedocs.io/en/latest/).

In order to perform the steps in this section you will need to:
1. Have [Protégé](https://protege.stanford.edu/) installed
2. Have a clone of your forked repository in your computer


Open Protégé. Click on `File`, `Open…`, and find the `abbreviation_for_your_ontology-edit.owl` file (e.g., `GitHub/abbreviation_for_your_ontology/src/ontology/abbreviation_for_your_ontology-edit.owl`

In my computer, this is
`GitHub/aism/src/ontology/aism-edit.owl`


### Explore the ontology and its hierarchy by clicking the entities tab in the top left area: ###


![ProtegeHome](https://github.com/insect-morphology/Manual/blob/main/img/ProtegeHome.png)


This will show you the main features that you will be working with:
- The **classes** window (left block, outlined in blue), where you can see the hierarchy
- The **annotations** window (top box on the right, outlined in green)
- **Description** window (bottom box on the right, outlined in pink)
- Annotation properties tab (top left, red arrow)
- **Object properties** tab (top left, yellow arrow)


![ProtegeMain](https://github.com/insect-morphology/Manual/blob/main/img/ProtegeMain.png)


## Setup Protégé to auto generate IRI-s ##

At the top menu: `Protégé` > `Preferences` > `New entities`

Apply the following settings:


![ProtegeEntityPref](https://github.com/insect-morphology/Manual/blob/main/img/ProtegeEntityPref.png)


**Entity IRI:**

Start with: Specified IRI: http://purl.obolibrary.org/obo 

Followed by: /

End with: Auto-generated ID


**Entity Label:**

Same as label renderer: IRI: http://www.w3.org/2000/01/rdf-schema#label
Lang: en

**Auto-generated ID:**

Numeric

Prefix AISM_

Suffix: leave this blank

Digit Count: 7

Start: Use the first number of **your assigned ID range***

End: Use the first number of **your assigned ID range***

Remember last ID between Protege sessions: **ALWAYS CHECK THIS**


**Note:** As every ID number must be unique within the ontology, you want the ID to be remembered by Protégé to prevent conflicts with your own ID’s. You will avoid conflicts with changes by other editors by using **your assigned ID range**). If you have not been assigned an ID range, please contact the appropriate ontology **manager** to set this for you.
