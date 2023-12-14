#Constructing a phylogenetic tree for the copper amine oxidase gene family in Arabidopsis thaliana
 
**Brief explanation of the data and analysis:**
The working annotated code that I've uploaded will make a fasta file,
containing the coding sequence for the 10 copper amine oxidase genes in the gene family.
The FASTA file made containing these sequences were uploadedand aligned using the web based tool MUSLCE 
(https://www.ebi.ac.uk/Tools/msa/muscle/). 
The aligned sequence was then downloded by running Python code, 
and the aligned sequence was used to make a phylogenetic tree using Neighbour-Joinin Model.
The aim is to see the evolutionary relationship between these genes. 

**To run the code:**
You will need the following libraries. Code to import them are as follows:
from Bio import Phylo
from Bio.Seq import Seq 
from Bio import SeqIO
from Bio.SeqRecord import SeqRecord
from Bio.Phylo.TreeConstruction import DistanceCalculator
from Bio.Phylo.TreeConstruction import DistanceTreeCalculator
from Bio import AlignIO 

**The output:**
A neighbour joining phylogenetic tree should be created as a result of running the code.
Details of what the tree should look like is as follows:
- zeta should be the most divergent from all the other sequences, 
  with epsilon 2 being the next most diversgent 
- the remaining gene sequences should form 2 clusters/groups:
   - group 1: alpha 1, alpha 2, apha 3, and beta
   - group 2: delta, epsilon 1, gamma 1, and gamma 2

