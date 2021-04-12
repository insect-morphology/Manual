# Manage and maintain the idranges file #

The ID ranges file is located within `src/ontology/` and its purpose is to help designating particular series of numbers to particular users and keep track of who would be using which numbers. This is a task for the order-specific ontology manager, who should set id ranges for each user by editing the `abbreviation_for_your_ontology-idranges.owl` file, keeping in mind that each term to be incorporated into the ontology must have a UNIQUE identifier, so id ranges per person must not overlap. If a number is used twice to designate terms, it will cause problems at the time of merging contributed edits. 

This is a relatively simple, but critical task during ontology development. Add the name of the person and their designated ranges of numbers as in the following example ID ranges files:

Gene Ontology (GO): https://github.com/geneontology/go-ontology/blob/master/src/ontology/go-idranges.owl

Cell Ontology (covoc)
https://github.com/obophenotype/cell-ontology/blob/master/src/ontology/cl-idranges.owl 

Anatomy of Insect SkeletoMuscular system (AISM): https://github.com/insect-morphology/aism/blob/master/src/ontology/aism-idranges.owl 

If you are a new contributor/editor for an order-specific ontology, please contact the main **manager** of the order-specific ontology (who should be identified in the initial `README.md` file in the ontology repository at [insect-morphology](https://github.com/insect-morphology)) so that they can assign you an ID range.
