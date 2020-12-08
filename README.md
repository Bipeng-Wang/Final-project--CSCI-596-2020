# Final-project--CSCI-596-2020

# Predicting Linear Free Energy Relationships in Substituted Benzoic Acid

## 1. Goal

#### Using machine learning (ML) to predict Hammett parameters of substituted benzoic acid. We first trained the random forest model and then compared the result with the neural network model.  

## 2. What is the Hammett parameter?

#### A Hammett parameter is a number describing how difficult a benzoic acid molecule dissociats in a certain solution to produce a corresponding benzoate and a proton. The equation of Hammett parameter first comes from experiments, which is given by:

![Figure1](https://user-images.githubusercontent.com/38379489/99776533-d6775200-2ac5-11eb-9556-a9750916c3d8.png)

## 3. Linear relationship between Hammett parameters and free energy changes

![Figure2](https://user-images.githubusercontent.com/38379489/99776844-51d90380-2ac6-11eb-8312-2b16594af118.png)

#### The two dissociation reactions above provide free energy changes which are related to equilibrium constants. The relation is given by:

![Figure3](https://user-images.githubusercontent.com/38379489/99776852-54d3f400-2ac6-11eb-860e-f9d79d93fcac.png)

#### When this equation is substituted into the first equation, the following equation is obtained:

![Figure4](https://user-images.githubusercontent.com/38379489/99776859-57cee480-2ac6-11eb-8774-16c78ddaaa01.png)

## 4. Extended-Connectivity Fingerprints (ECFP)

#### The fingerprint called ECFP is used as input. It is a type of circular topological fingerprints recording the neighborhood of each non-hydrogen atom into multiple circular layers up to a given diameter. These atom-centered sub structural features are then mapped into integer codes using a hashing procedure.

Examples of 16 bits fingerprints:

| CH3-p | 0 | 1 | 1 | 1 | 0 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| NH2-m | 1 | 1 | 1 | 0 | 0 | 1 | 0 | 0 | 1 | 1 | 1 | 1 | 0 | 1 | 0 | 1 |
| F-p | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 0 | 0 | 1 | 0 | 1 | 0 | 0 | 0 |

## 5. Random forest

#### Random forest is an ensemble machine learning model consisting a user-defined number of decision trees. The results of random forests are obtained from vote (classification) or average (regression).The bootstrap sampling method is used to select subsets of database.

![Figure5](https://user-images.githubusercontent.com/38379489/99776864-59001180-2ac6-11eb-9674-6668ca75f94e.png)

## 6. Training result 
#### Random forest
![fig](https://user-images.githubusercontent.com/38379489/101554614-d56e6d80-396b-11eb-9ba6-711af97f24af.png)

#### NN model
![1607471513420](https://user-images.githubusercontent.com/38379489/101555367-63972380-396d-11eb-866a-0a2866561039.png)

