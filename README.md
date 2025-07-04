Cite as: ![image](https://github.com/user-attachments/assets/7290ba1d-9f31-4ac5-836b-8d74ad38abcf)


# def-au-asls-land-surface

Preparation and maintenance of a machine-readable representation of the classifiers described in chapter 7 Land Surface, by R.C. McDonald, R.F. Isbell and J.G. Speight, in Australian soil and land survey field handbook (3rd edn)

## Preparing the vocabulary for loading in RVA

All collection members must have an `rdf:type`, else they won't render in the RVA browse view. 
All resources must have an `rdfs:label` or `skos:prefLabel`, else they won't have nice titles in the RVA browse view. 

Since `ASLS Land Surface` imports some concepts and collections from `ASLS Substrate`, the `rdf:type` and `skos:prefLabel` for the linked elements must be available locally, not just through the `owl:imports`. 

Run this SPARQL prior to loading:
```
INSERT  { ?m a ?t ; skos:prefLabel ?l .}
WHERE {
	?c skos:member ?m . 
	?m a ?t ; 
	      skos:prefLabel ?l .
}
```

Contact: 

Linda Gregory
linda.gregory@csiro.au 

Simon Cox
simon.cox@csiro.au
