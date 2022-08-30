# Bell
The Bell ontology module of the [Polifonia ontology network](https://github.com/polifonia-project/ontology-network) represents concepts and relationships to describe bells, bell towers and bell ringers.

## Competency questions addressed by this ontology module
- Where is the building/church/bell tower?
- When (what year) was the building built?
- In which context is the building located (urban, periurban...)?
- Are there bells in the church? How many bells are in the church?
- Which is the material of the bell?
- By whom (by which foundry) were they melted?
- In which year were they melted?
- Which is the weight of the bell?
- Which are the measures of the bell?

## Competency questions that will be addressed by this ontology module
- Which is the mounting system of the bell?
- Which is the nominal/fundamental note of the bell?
- Which is the extension of the whole set of bells in a bell tower?
- What kind of execution techniques are possible to perform according to a specific mounting system?
- Can a set of bells be played electrically, manually, or both?
- How/Using which tools/Using which execution technique(s) is the set of bells played, when played manually?
- TO BE COMPLETED

## Imported ontologies

### External Imports
- [ArCo Ontology network](https://w3id.org/arco/ontology/arco)

## Ontology Description

This ontology makes it possible to describe bells, bell towers and bell ringers.
It reuses and will extend ArCo ontology network.

## Datasets
Data about two sets of bells, modelled according to the imported ArCo ontology network, have been published so far:
- https://w3id.org/arco/resource/MusicHeritage/0700377972-0 (68 triples)
- https://w3id.org/arco/resource/MusicHeritage/0700377973-0 (68 triples)

Relevant properties describing a set of bells are:
- arco:numberOfComponents (how many bells are in the church?)
- a-loc:hasTimeIndexedTypedLocation (are there bells in the church?)
- a-dd:hasMaterial (which is the material of the bell?)
- a-cd:hasAuthor / a-cd:hasPreferredAuthor / a-cd:hasAuthorshipAttribution (by whom (by which foundry) were they melted?)
- a-cd:hasDating (in which year were they melted?)
- a-dd:hasMeasurementCollection (which is the weight of the bell?, which are the measures of the bell?)

***License***: Attribution-ShareAlike 4.0 International https://creativecommons.org/licenses/by-sa/4.0/
