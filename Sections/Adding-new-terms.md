# Adding new terms #

Open your `ontology-edit.owl` file.

First of all, make sure that the term that you are about to add **DOES NOT** exist in the ontology yet. 

This can be done by searching the term: go to `Edit` on the top menu and then `Find`, which will open the `Search` window. Start typing the term. The program will start showing the terms that contain the combination of letters that you are typing.

<img src="https://github.com/insect-morphology/Manual/blob/main/img/ProtegeSearch.png" alt="ProtegeSearch" width="80%"/>

**Note:** In AISM, we tried our best to name combined terms from dorsal to ventral (e.g., noto-pleural conjunctiva) or proximal to distal (e.g., pleuro-coxal muscle), but just in case, make sure to search for both options (i.e., pleuro-notal, coxo-pleural).

Once you have checked that the term is not currently included in the ontology, check for what would be the best parent for it. Main categories include 'sclerite', 'conjunctiva' (for membranes), both under 'region of cuticle', and 'skeletal muscle tissue' (for muscles).

<img src="https://github.com/insect-morphology/Manual/blob/main/img/ProtegePlace.png" alt="ProtegePlace" width="80%"/>

<img src="https://github.com/insect-morphology/Manual/blob/main/img/ProtegePlace2.png" alt="ProtegePlace2" width="80%"/>

<img src="https://github.com/insect-morphology/Manual/blob/main/img/ProtegePlace3.png" alt="ProtegePlace3" width="80%"/>

Click on the appropriate parent category for your term so that it is highlighted in blue, and then click on the 'Add class' icon, which is the first one on the top left corner of the Classes window.

<img src="https://github.com/insect-morphology/Manual/blob/main/img/ProtegeAdd.png" alt="ProtegeAdd" width="60%"/>

This will open a new window where you can type your new term, and Protégé will automatically generate the appropriate number for it, given that you set it up for this (see [set up Protégé to auto generate IRI-s](https://github.com/insect-morphology/Manual/blob/main/Sections/Setup-Protege.md)). Then click

<img src="https://github.com/insect-morphology/Manual/blob/main/img/ProtegeNewClass.png" alt="ProtegeNewClass" width="80%"/>


The newly added term will now be listed in the annotations window. Each new term should be annotated with the following information:

- The **name (rdfs:label)** should be annotated with the language of the term (en) and at least one **"sensu"**, which should include a reference with a DOI or a link to where this reference can be found, and the textual definition of the term according to that particular reference.
- A **definition**, ideally created from the subclasses added to the term, which should include the **contributor** who created the definition and the **creation_date** of this definition.

----------------------

# Adding annotations #

### Sensu ###

To add annotations to an existing term click on the `@` symbol on the right side of the annotations tab, opposite to where the `rdfs:label` is. 

<img src="https://github.com/insect-morphology/Manual/blob/main/img/ProtegeAnnotation.png" alt="ProtegeAnnotation" width="80%"/>

This will open the `Annotations for AnnotationAssertion` window to choose what kind of annotation will be added. Click on the plus sign, which opens the `Create annotation` window.

<img src="https://github.com/insect-morphology/Manual/blob/main/img/ProtegeAnnAnn.png" alt="ProtegeAnnAnn" width="60%"/>

Scroll down the list of **'Annotation properties'** to find `subset_property` and within that list find an click on `sensu`. On the right side panel, add:
- The full bibliographic reference from the publication that you are taking this textual definition from.
- The DOI or a URL link for this bibliographic reference.
- In quotation marks, the textual verbatim definition for the term, as presented in this bibliographic resource. 

Choose the appropriate language for this definition and click OK.

<img src="https://github.com/insect-morphology/Manual/blob/main/img/ProtegeAnnSensu.png" alt="ProtegeAnnSensu" width="80%"/>

This will take you back to the `Annotations for AnnotationAssertion` window, which will show you the content you just added. There you press `OK`.

<img src="https://github.com/insect-morphology/Manual/blob/main/img/ProtegeAnnAnn2.png" alt="ProtegeAnnAnn2" width="60%"/>

And this will take you back to tha main ontology view, where your newly added annotations will show under the `rdfs:label`, and the `@` symbol will now appear in yellow.

<img src="https://github.com/insect-morphology/Manual/blob/main/img/ProtegeAnnAnn3.png" alt="ProtegeAnnAnn3" width="80%"/>


----------------------

### SubClass Of ###



----------------------

### Definition ###