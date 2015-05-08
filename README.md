# aop-ontology
Ontology to manage adverse outcome pathways and associated data for predictive toxicology

##Description
The intent of the Adverse Outcome Pathway Ontology (AOPO) are to provide:
  * Semantic NoSQL way of accessing and managing Adverse Outcome Pathways (AOP)
  * Ways and means to facilitate computation on data within the OECD AOP-Wiki
  * Ways and means to standardize the lingua franca of the OECD AOP-Wiki
  * The data framework to enable the development of artificial intelligence for predictive toxicology
  * A central depository of toxicological knowledge to facilitate rapid and more efficient risk assessment

The AOPO consists of an OWL file that contains information from various sources. These sources currently include:
  * OECD AOP-Wiki
  * ChEBI (and its dependencies)
  * Human Phenotype Ontology (and its dependencies)
  * Bioassay Ontology (and its depenedencies)

Future sources will include:
  * NCBI PubChem
  * EPA ToxCast
  * NIH/FDA/EPA Tox21
  * Others (by nomination or that we identify)

##Contributing
If you'd like to contribute please contact the maintainer first.

##Usage
The contents of the OWL file can be used in the same way any OWL file can. Note that we intend computation, inference, and the like to be performed at the individual level. So, for instance, we may have a class called RAR (retinoic acid receptor). That class defines an individual protein called by rar. When we are associating the protein rar with an individual assay that has data, we will use the rar individual. Likewise, for any given AOP, we use individuals as key events and other AOP entities to construct the realization of a given AOP.
