# Setup Protégé to auto generate IRI-s #

Open your `ontology-edit.owl` file.

At the top menu: `Protégé` > `Preferences` > `New entities`

Apply the following settings:


<img src="https://github.com/insect-morphology/Manual/blob/main/img/ProtegeEntityPref.png" alt="ProtegeEntityPref" width="80%"/>


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

Next, you can either [import existing terms](https://github.com/insect-morphology/Manual/blob/main/Sections/Setup-Protege.md) from other ontologies, if needed, or you can [add new terms](https://github.com/insect-morphology/Manual/blob/main/Sections/Adding-new-terms.md) to the current ontology, making sure to include all the necessary annotations.