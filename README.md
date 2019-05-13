# RFA: Recursive Feature Addition

Modified from the RFE code in this manner:
Instead of elimination the worst feature, the algorithm eliminates the best feature.
In the end of the process, instead or returning <ranking>, it will return <reverse(ranking)>
So that the first feature eliminated will be the most important one in the ranking.
The core idea in this process is to maintain correlated proteins close to each other.

For instance, in proteomics data sets, if two proteins are 
highly correlated, the RFE may remove one of them in the middle of the elimination process
and let the other be positioned in the beggining of the rank.
RFA gets the best feature and put it in the beggining of the rank, then, if a protein is 
very similar to this one, it is expected that the RFA will select this 
in the following iteration(s).

RFA is a prototype and needs to be assessed. In my doctorate, I have tested with only one dataset and it demonstrated to position the controlled True Positive important-features, candidate biomarkers, more consistently, also being more stable among cross-validation iterations.

![](https://github.com/heberleh/recursive-feature-addition/blob/master/img/dcv_rfe_vs_rfa.png)


**Please cite** my work, go to section **[Citation](#citation)**


Author of RFA code: 

         Henry Heberle <https://github.com/heberleh>

Authors of RFE code - From Sklearn: 
         Alexandre Gramfort <alexandre.gramfort@inria.fr>
         Vincent Michel <vincent.michel@inria.fr>
         Gilles Louppe <g.louppe@gmail.com>
License: 
         BSD 3 clause



# Citation

[1] H. Heberle, “Computational methods in Biology: cancer biomarkers, protein networks and lateral gene transfer,” University of São Paulo, 2019.

1. Heberle, H. Computational methods in Biology: cancer biomarkers, protein networks and lateral gene transfer. (University of São Paulo, 2019).

```bibtex
@phdthesis{Heberle2019,
    author = {Heberle, Henry},
    pages = {164},
    school = {University of S{\~{a}}o Paulo},
    title = {{Computational methods in Biology: cancer biomarkers, protein networks and lateral gene transfer}},
    type = {Doctoral Dissertation},
    year = {2019}
}
```
