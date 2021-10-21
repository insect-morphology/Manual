# Using templates to edit and extend the AISM #

The AISM aims for definitions that follow consistent, simple patterns. 

Here we provide a template system that allows the user to:
- Provide a suggested term
- Provide a natural language definition
- Specify the kind of cuticular structure that the term is referring to (i.e. region of cuticle, sclerite, conjunctiva, cuticular protrusion, etc.)
- Indicate the location of the structure on the insect body
- Indicate other locators
- Indicate composition

This template system can be used to suggest new insect anatomical terms that are missing from the AISM, or to extend the AISM to create taxon-specific ontologies.

Template example:

| ID      | TYPE             | description                                                                                                            | Label                | TAXON                | MoDIAS_type  | location            | laterality            | continuous_with             | adjacent_to             | posterior_to             | anterior_to              | dorsal to             | ventral to             | lateral to           | has_part             |
|---------|------------------|------------------------------------------------------------------------------------------------------------------------|----------------------|----------------------|--------------|---------------------|-----------------------|-----------------------------|-------------------------|--------------------------|--------------------------|-----------------------|------------------------|----------------------|----------------------|
| ID      | TYPE             | A rdfs:comment                                                                                                         | A rdfs:label         | TI 'in taxon' some % | TI %         | TI 'part of' some % | TI 'bearer of' some % | TI 'continuous with' some % | TI 'adjacent to' some % | TI 'posterior to' some % | TI 'anterior to' some  % | TI 'dorsal to' some % | TI 'ventral to' some % | TI lateral_to some % | TI 'has_part' some % |
| EX:2260 | named individual | The paired protrusion of the dorsal region of the postabdomen that is anterior to the anus and composed of cercomeres. | cercus_Archaeognatha | NCBITaxon:29994	      | AISM:0000008 | AISM:0000523        | PATO:0040024          |                             |                         |                          | AISM:0004197             |                       |                        |                      | AISM:0004199         |

This template can be easily converted into an OWL file by using ROBOT functions (http://robot.obolibrary.org/template for reference). This OWL file can be merged with the AISM at any point.
