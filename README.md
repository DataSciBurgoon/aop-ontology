# Development Philosophy

The development philosophy is an object-oriented approach. Classes represent a class of objects -- the general properties are laid out here. Individuals represent objects, or instantiations of the class. This was done so that we can handle individual cases of assays. This design decision has ramifications -- we had to implement this design also with the AOPs as well.

# Assays --> Adverse Outcomes (Predictive Tox)

In vitro assays are handled using BAO. Thus, the "measure group" under "assay bioassay component" holds the relationship between a chemical (via 'has participant') and the key event component or key event (via a different 'has participant').

# Adverse Outcome Pathways and Sufficient Relationships

Because our goal is to make computational toxicology predictions based on existing toxicological and disease knowledge, we define adverse outcomes as being equivalent to having activation or inactivation/deactivaion of some key event. For instance, has_inactivated_key_event some HSD17B4 is sufficient to infer a chemical causes steatosis (AO-Steatosis under AopEntity | AdverseOutcome | LiverAdverseOutcome). This is encoded in the "Equivalent To" slot in AO-Steatosis.

Sufficient relationships can be defined on existing biological knowledge (e.g., inhibition of PTGS1 and PTGS2 is sufficient according to the literature to know that a chemical will cause gastric ulcers), or based on causal network theory (i.e., if AOPs are causal chains, then causal network theory can be used to identify sufficient relationships).

# Results from Computer Models

We have results from in vitro assays being handled by BAO. We will need to create new classes in the future to handle results from computer models.

# Results from in vivo Models

We are currently working out an ontology to help us capture data from in vivo models.
