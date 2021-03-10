# Welcome to StrainHub!

## About StrainHub

StrainHub is designed as a web-based software to generate disease transmission networks and associated metrics from a combination of a phylogenetic tree and associated metadata. Today, StrainHub consists of a standalone R package, a code-free web application, and a containerized version for running the web app locally.

The software maps the metadata onto the tree and performs a parsimony ancestry reconstruction step to create links between the associated metadata and enable the construction of the network. Users have the option to build a tree utilizing their method of preference outside StrainHub or build a tree utilizing a FASTA file within StrainHub with the Neighbor-Joining algorithm.

Alternatively, the user can skip the StrainHub ancestry reconstruction step by generating a maximum clade credibility tree \(MCC\) through BEAST phylogeography or input a previously generated list of edges in order to build the transmission network. Additionally, the user can input a file with geographic cooordinates associated with the character of interest and have the network plotted into a map.



