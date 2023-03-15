# Bell
The Bell ontology module of the [Polifonia ontology network](https://github.com/polifonia-project/ontology-network) (PON) represents concepts and relationships to describe bells, bell towers and bell ringers.

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
- When were they melted?
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

## Examples of SPARQL queries addressed by the module
- By whom (by which foundry) were the bell(s) melted? When where they melted?
```
PREFIX tiapit: <https://w3id.org/italia/onto/TI/>
PREFIX core: <https://w3id.org/arco/ontology/core/>
PREFIX a-cd: <https://w3id.org/arco/ontology/context-description/>
PREFIX arco: <https://w3id.org/arco/ontology/arco/>
SELECT DISTINCT ?bell ?desc ?author ?authorLab ?dating ?datingTime
WHERE { ?bell arco:isCulturalPropertyComponentOf ?setofbells ; rdf:type arco:MusicHeritage ;
core:description ?desc ;
a-cd:hasDating ?dating ;
a-cd:hasAuthor ?author ;
dc:subject ?o .
?author rdfs:label ?authorLab .
?dating a-cd:hasDatingEvent ?datingEv .
?datingEv tiapit:atTime ?datingTime
FILTER(str(?o)='campana')
}
```

- Are there bells in the church/bell tower?
```
PREFIX tiapit: <https://w3id.org/italia/onto/TI/>
PREFIX core: <https://w3id.org/arco/ontology/core/>
PREFIX a-cd: <https://w3id.org/arco/ontology/context-description/>
PREFIX arco: <https://w3id.org/arco/ontology/arco/>
SELECT DISTINCT ?site ?siteLab ?bell ?desc
WHERE { ?bell arco:isCulturalPropertyComponentOf ?setofbells ; rdf:type arco:MusicHeritage ;
a-loc:hasTimeIndexedTypedLocation ?titl ;
core:description ?desc ;
dc:subject ?o .
?titl a-loc:atSite ?site .
?site rdfs:label ?siteLab
FILTER(str(?o)='campana')
}
```

- Which is the weight of the bell?
```
PREFIX tiapit: <https://w3id.org/italia/onto/TI/>
PREFIX muapit: <https://w3id.org/italia/onto/MU/>
PREFIX core: <https://w3id.org/arco/ontology/core/>
PREFIX a-cd: <https://w3id.org/arco/ontology/context-description/>
PREFIX arco: <https://w3id.org/arco/ontology/arco/>
PREFIX a-dd: <https://w3id.org/arco/ontology/denotative-description/>
SELECT DISTINCT ?bell ?desc ?m ?mLab ?v ?u ?uLab
WHERE { ?bell arco:isCulturalPropertyComponentOf ?setofbells ; rdf:type arco:MusicHeritage ;
a-loc:hasTimeIndexedTypedLocation ?titl ;
core:description ?desc ;
a-dd:hasMeasurementCollection ?mc ;
dc:subject ?o .
?mc a-dd:hasMeasurement ?m .
?m a-dd:hasMeasurementType a-dd:Weight .
?m rdfs:label ?mLab ; a-dd:hasValue ?mVal .
?mVal muapit:value ?v ; muapit:hasMeasurementUnit ?u .
?u rdfs:label ?uLab
FILTER(str(?o)='campana')
}
```

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
