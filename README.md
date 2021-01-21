# How to create insect anatomy ontologies using the Ontology Development Kit (ODK) and edit them in Protégé 

A manual edited by [Jennifer C. Girón](https://github.com/JCGiron) and [István Mikó](https://github.com/teleaslamellatus)
January 2021

## Background

We created an ontology for the anatomy of the insect skeletomuscular system [AISM](https://github.com/insect-morphology/aism) using the Ontology Development Kit [ODK](https://github.com/INCATools/ontology-development-kit). The ODK provides a standardized system to create, manage, release and edit ontologies to maximize interoperability among them (i. e., ability to reuse terms from existing ontologies; more details at https://douroucouli.wordpress.com/2018/08/06/new-version-of-ontology-development-kit-now-with-docker-support/) and facilitate collaborative editing using GitHub. 

The AISM contains all the basic terms shared across insects, along with relationships and annotation options, with the idea that it serves as a base for order-specific insect anatomy ontologies that incorporate order-specific terms. So the idea with the AISM is to provide a backbone and headstart for order-specific ontologies.

Because of the way that ODK imports pre-existing terms, the full AISM can be overwhelming for first-time users, as it includes all the terms and relationships inherited from multiple hierarchies from other ontologies involved (i.e. [BFO](http://www.obofoundry.org/ontology/bfo.html), [BSPO](http://www.obofoundry.org/ontology/bspo.html), [PATO](http://www.obofoundry.org/ontology/pato.html), [RO](http://www.obofoundry.org/ontology/ro.html), [UBERON](http://www.obofoundry.org/ontology/uberon.html)). That is why a **_simplified version of the AISM**_ is provided and should be the start point for any future insect order-specific ontologies. This version includes essential relationships and annotation properties as well as basic insect-specific terms.

We provide here instructions for creating ontologies using this **_simplified version of the AISM**_.

## Initial thoughts for order-specific ontologies

Given that the AISM already contains basic terms and definitions for Insecta, the main goal of order-specific ontologies would be to gather order-specific terminology.

The way we are doing this for the Coleoptera Anatomy Ontology project [COLAO](https://github.com/insect-morphology/colao) is by getting all the most broadly accepted beetle terms and definitions from Lawrence and Ślipiński (2013; Adult morphology. In: Australian beetles volume 1: morphology, classification and keys. CSIRO Publishing, p. 30–63), and for now, adding them to a team-shared spreadsheet. Once we get those terms incorporated into the ontology file, we will be adding additional terms traditionally used, annotating whether those are synonyms of the more broadly accepted terms. We will also add terms from specialized morphological works on different skeletal systems in order to increase and refine the knowledge base.

**Defining name and ID for order-specific ontologies**: We invite you to read through the [Principles](http://www.obofoundry.org/principles/fp-000-summary.html) established by the [OBO Foundry](http://www.obofoundry.org/about-OBO-Foundry.html), the organization working to build tools and standards to maintain and increase interoperability across ontologies. Specifically dealing with ontology names is [Principle 3](http://www.obofoundry.org/principles/fp-003-uris.html) and the [recommendations](http://www.obofoundry.org/id-policy) therein. 

For now, once you define an ID, which will be the prefix for all your unique identifiers and the acronym for your order-specific ontology, just make sure that this ID is not listed on the [main OBO Foundry page](http://www.obofoundry.org/). Once you have a first release version of your ontology you will need to officially request the name space by issuing a [New Ontology Request](https://github.com/OBOFoundry/OBOFoundry.github.io/issues/new?assignees=&labels=new+ontology&template=new-ontology-request.md&title=) via Issue Tracking in GitHub (see also the available [instructions](http://obofoundry.org/docs/NewOntologyRegistrationInstructions.html) for this).
