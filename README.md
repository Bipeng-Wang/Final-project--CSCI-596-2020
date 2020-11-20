# Final-project--CSCI-596-2020

**Predicting Linear Free Energy Relationships in Substituted Benzoic Acid**

1. Goal

Build a machine learning model to predict Hammett parameters of substituted benzoic acid.

1. What is the Hammett parameter?

A Hammett parameter is a number describing how difficult a benzoic acid molecule dissociats in a certain solution to produce a corresponding benzoate and a proton. The equation of Hammett parameter first comes from experiments, which is given by:

 ![](RackMultipart20201120-4-e2aa6k_html_fb42ae124126cbc8.gif)

1. Linear relationship between Hammett parameters and free energy changes

 ![](RackMultipart20201120-4-e2aa6k_html_9c21d0533dcbb2b8.gif)

![](RackMultipart20201120-4-e2aa6k_html_8191e34e48350ea8.gif)

The two dissociation reactions above provide free energy changes which are related to equilibrium constants. The relation is given by:

When this equation is substituted into the first equation, the following equation is obtained:

![](RackMultipart20201120-4-e2aa6k_html_adcd58fed2679c6b.gif)

1. Extended-Connectivity Fingerprints (ECFP)

The fingerprint called ECFP is used as input. It is a type of circular topological fingerprints recording the neighborhood of each non-hydrogen atom into multiple circular layers up to a given diameter. These atom-centered sub structural features are then mapped into integer codes using a hashing procedure.

Examples of 16 bits fingerprints:

| CH3-p | 0 | 1 | 1 | 1 | 0 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| NH2-m | 1 | 1 | 1 | 0 | 0 | 1 | 0 | 0 | 1 | 1 | 1 | 1 | 0 | 1 | 0 | 1 |
| F-p | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 0 | 0 | 1 | 0 | 1 | 0 | 0 | 0 |

1. Random forest

Random forest is an ensemble machine learning model consisting a user-defined number of decision trees. The results of random forests are obtained from vote (classification) or average (regression).The bootstrap sampling method is used to select subsets of database.

![](RackMultipart20201120-4-e2aa6k_html_eefeb336a48f61ba.gif)
