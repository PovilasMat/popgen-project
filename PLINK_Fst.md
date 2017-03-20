# Calculate Fst with PLINK

Create a new directory called `Fst` to store output files

```
mkdir Fst
```

##Fst between localities


```
plink --bfile locality_grants --fst --within ../locality_clusters_no_outgroup.txt -out Fst/Fst_locality_no_outgroup
```

Result
```
--within: 13 clusters loaded, covering a total of 88 people.

...

Mean Fst estimate: 0.282646
Weighted Fst estimate: 0.310916
```

*NB 4 unknown samples were not included in the analysis somehow. Bug?*


### Fst between species

```
plink --bfile species_grants --fst --within ../species_clusters_no_outgroup.txt -out Fst/Fst_species_no_outgroup
```

Result
```
--within: 4 clusters loaded, covering a total of 92 people.

...

Mean Fst estimate: 0.254961
Weighted Fst estimate: 0.2885
```