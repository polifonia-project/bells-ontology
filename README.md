# Bell
The Bell ontology module of the [Polifonia ontology network](https://github.com/polifonia-project/ontology-network) represents concepts and relationships to describe bells, bell towers and bell ringers.

## Ontology Description

This ontology makes it possible to describe bells, bell towers and bell ringers.
Bells, which are the main subject of this module, are described by means of measurable, intrinsic aspects such as weight, materials, conservation status, as well as properties deriving from interpretation situations, such as authorship attribution, dating, execution techniques, and their related objects (e.g. bibliography).
The Bell ontology modules reuses and extends the ArCo ontology network.

<img width="809" alt="bell-ontology" src="https://user-images.githubusercontent.com/36740200/211186880-37d4c9ec-877e-44ad-bd77-a1e5863d54bb.png">


## Competency questions addressed by this ontology module
- Where is the building/church/bell tower?
- When (what year) was the building built?
- In which context is the building located (urban, periurban...)?
- Are there bells in the church/bell tower? How many bells are in the church/bell tower?
- Is there a single bell or a poliorganic instrument (a set of bells) in a church/bell tower?
- By whom (by which foundry) were they melted?
- In which year were they melted?
- Which is the material of the bell?
- Which is the weight of the bell?
- Which are the measures of the bell?

## Competency questions that will be addressed by this ontology module
- Is the bell tower associated to a religious building or a civil building?
- Which is the mounting system of the bell?
- Which is the nominal/fundamental note of the bell?
- Which is the extension of the whole set of bells in a bell tower?
- What kind of execution techniques are possible to perform according to a specific mounting system?
- Can a set of bells be played electrically, manually, or both?
- Is the sound in a place currently performed by hand or by electric means?
- How/Using which tools/Using which execution technique(s)/Following which sound practices is the set of bells played, when played manually?
- What are the recordings involving a bell or set of bells?

## Imported ontologies

### External Imports
- [ArCo Ontology network](https://w3id.org/arco/ontology/arco)


## Statistics
Considering that, apart from the definition of some novel classes inside the module (such as Bell, SetOfBells, and BellTower), the BELL module widely relies on the ArCo ontology network, we report here useful statistics of ArCo: 
- number of classes: 340 
- number of object properties: 616
- number of datatype properties: 154
- number of logical axioms: 3,416

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
