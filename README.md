## BIOHACK-2018 project: Towards TCR specificity prediction

### Data

The repository contains the following datasets:

- `vdjdb.txt` in root folder is a filtered sample from VDJdb database (Human TCR beta, only epitopes represented by 30+ sequences)
- `vdjdb/` folder contains full database in two formats (slim and wide) and includes all avilable epitopes for TCR alpha and beta from human, mouse and monkey.

> For more details on VDJdb format see https://github.com/antigenomics/vdjdb-db/blob/master/README.md

- `samples/` folder contains TCR beta RepSeq data from two donors. `M` and `N` suffices highlight memory and naive T-cells respectively. Donor9 is CMV+ and Donor7 is CMV-.

> For more details on RepSeq data format see http://vdjtools-doc.readthedocs.io/en/latest/input.html#clonotype-tables

And miscellaneous data:

- `alignment_matrix/` folder contains BLOSUM62 and VDJAM substitution scoring matrices, the latter is optimized for CDR3
- `segments/` folder contains Variable segment sequences and segment alignment scores

### Objectives

Main objectives of this project are (from simple to hard):

- Build custom classifiers for TCR sequences specific to selected epitopes, e.g. A02-NLV-specific TCR beta classifier
- Perform dimensionality reduction and visualization of VDJdb database using state-of-art methods e.g. [Flt-SNE](https://github.com/KlugerLab/FIt-SNE)
- Design a TCR sequence similarity metric. Can be both alignment-based and K-mer match based. Run unsupervised clustering using this metric and see if it fits epitope specificity landscape.
- Develop a generalized classifier that uses both TCR and epitope sequence/sub-sequences and is trained for whole VDJdb dataset

> Overview and introduction can be found in bh2018_full_slides.pdf in root folder
