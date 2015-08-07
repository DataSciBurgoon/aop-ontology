# How to build an AOP

The general process is that an AOP is actually going to be an instance of a particular subclass of AdverseOutcomePathway. For instance, the AOP 'AOP Neural Tube Defect via Hoxb1' is an instance, member, or individual, of the class NeuralTubeDefect, which is itself a subclass of DevelopmentalToxicologyAOP, which is itself a subclass of AdverseOutcomePathway.

## Naming Conventions:
### AOP Naming Convention
All instances of an AOP must begin with the word 'AOP'. For instance, an AOP for steatosis via HSD17B4 inactivation would be named 'AOP Steatosis Via HSD17B4'.

## Some Important Concepts
### AdverseOutcomePathways As Containers
The best way to think of AdverseOutcomePathway instances is that they are containers of has\_key\_event_relationship and has\_chemical\_mie\_relationship triples (where the subject is the AOP). AOP Neural Tube Defect via Hoxb1, an instance of NeuralTubeDefect, is a good example. 

### AdverseOutcomePathways Must Have rdfs:labels
In general, everything in the AOPO should have rdfs:labels. This is a housekeeping item that we need to fix in future releases. However, it is *IMPERATIVE* that AdverseOutcomePathways always have rdfs:labels -- if they don't, they will not show up in the AOPXplorer (speaking from experience).

## Creating an AOP: Step-by-Step and From Scratch
1. Create a new AdverseOutcomePathway class for your AOP if one doesn't already exist. Keep in mind that we are trying to create a hierarchy, so make a more generalized class if appropriate. Your AOP is going to be an instance of a more general class of AOPs. So, for instance, we have a NeuralTubeDefect class, and it has a specific AOP (an individual or instance) called 'AOP Neural Tube Defect via Hoxb1'.
2. All AOPs _should_ have entries (and these entries need to be indvididuals or instances of a class) for the following:
    *  has\_confidence some Confidence
    *  has\_adverseoutcome exactly 1 AdverseOutcome
    *  has\_aop_relationship some AOPRelationship
    *  has\_chemical\_mie_relationship exactly 1 ChemicalMIERelationship
3. In addition, AOPs _should_ have entries (again, these entries need to be individuals or instances of classes) for any other relationships that are inherited from any specific subclass of AdverseOutcomePathway.
4. If individuals do not exist for your entries for steps 2 and 3, then you should create them.
5. Create individuals for the key events, key event relationships, and chemical MIE relationships. Reuse individuals when possible.
6. Within the AOP individual, create the object propery assertions for the key event relationships and the mie chemical relationship.
7. 
