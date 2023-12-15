#Constructing a phylogenetic tree using neighbour joining model,
#for the copper amine oxidase gene family in Arabidopsis thaliana
 
**Brief explanation of the data and analysis:**
The aim of this investigation, is to look into the evolutionary relationship of these genes.

The working annotated code that I've uploaded will make a fasta file
containing the coding sequence (obtained from TAIR)
for the 10 copper amine oxidase genes in a gene family.

The FASTA file made containing these sequences were uploaded
and aligned using the web based tool MUSLCE (https://www.ebi.ac.uk/Tools/msa/muscle/). 

The aligned sequence was then downloded by running Python code, 
and the aligned sequence was used to make a phylogenetic tree using Neighbour-Joining Model.

**To run the code:**
Open the DataScience2.ipynb file in JupyterLab.

Code to import the necessary libraries are as follows:
from Bio import Phylo
from Bio.Seq import Seq 
from Bio import SeqIO
from Bio.SeqRecord import SeqRecord
from Bio.Phylo.TreeConstruction import DistanceCalculator
from Bio.Phylo.TreeConstruction import DistanceTreeCalculator
from Bio import AlignIO 

SeqRecord objects were made for the 10 coding sequences
along with its corresponding gene name and combined together into one record.
 - SeqRecord(
   Seq(
   ),
   id = , 
)

A file was then made of this record in FASTA format. 
 - SeqIO.write()

The FASTA file made was uploaded to MUSCLE, and the aligned sequence was downloaded into Python.
The url in the code can be changed to the url you get from aligning your sequence on MUSCLE. 
 - urllib.request.urlretrieve()


Distance matrix was calculated and a distance tree constrictor project was made.
 - DistanceCalculator()
 - calculator.get_distance()
 - DistanceTreeConstructor()

Phylogenetic tree using neighbour joining model was created and visualised.
 - constructor.nj()
 - Phylo.()
 - Phylo.draw_ascii()

**The output:**
A neighbour joining phylogenetic tree should be created as a result of running the code.
Details of what the tree should look like is as follows:
- CuAOzeta should be the most divergent from all the other sequences 
- the remaining gene sequences should form 2 clusters/groups:
   - group 1: CuAOepsilon2, CuAOalpha1, CuAOalpha2, CuAOalpha3, and CuAObeta
   - group 2: CuAOdelta, CuAOepsilon1, CuAOgamma1, and CuAOgamma2
