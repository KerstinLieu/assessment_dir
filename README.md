# Constructing a phylogenetic tree using neighbour joining model, for the copper amine oxidase gene family in Arabidopsis thaliana
 
**BRIEF EXPLANATION OF DATA AND ANALYSIS:**
The aim of this investigation, is to look into the evolutionary relationship of these genes.

The working annotated code that I've uploaded will make a fasta file
containing the coding sequence (obtained from TAIR database)
for the 10 copper amine oxidase genes in a gene family.

The FASTA file made containing these sequences were uploaded
and aligned using the web based tool MUSLCE (https://www.ebi.ac.uk/Tools/msa/muscle/). 

This aligned sequence was then downloded and then read by running Python code. 
The aligned sequence was used to make a phylogenetic tree using Neighbour-Joining Model.


**TO RUN THE CODE:**
Download zip file of the assessment_dir repository. Extract and move the extracted assessment_dir-main file into an appropriate location where you are able to and open the DataScience2.ipynb file in JupyterLab (Jupyter Notebook) from Anaconda Navigator.
Run code.

Code to import the necessary libraries are as follows (this is already written in the code):
from Bio import Phylo,
from Bio.Seq import Seq,
from Bio import SeqIO,
from Bio.SeqRecord import SeqRecord,
from Bio.Phylo.TreeConstruction import DistanceCalculator,
from Bio.Phylo.TreeConstruction import DistanceTreeCalculator,
from Bio import AlignIO, 

SeqRecord objects were made for the 10 coding sequences
along with its corresponding gene name and combined together into one record.
 - SeqRecord(
   Seq(
   ),
   id = , 
)

A file was then made of this record in FASTA format. 
 - SeqIO.write()

The FASTA file made was uploaded to MUSCLE, and the aligned sequence was downloaded as a clustal file named CLUSTAL_multiple_sequence_alignment.clw.
If the zip file of the repository was downloaded, the clustal file should be in the same directory as the code file (DataScience2.ipynb).
This file needs to be opened and read using this code:
with open("CLUSTAL_multiple_sequence_alignment.clw","r") as clw: 
    align = AlignIO.read(clw,"clustal")

Distance matrix was calculated and a distance tree constrictor project was made.
 - DistanceCalculator()
 - calculator.get_distance()
 - DistanceTreeConstructor()

Phylogenetic tree using neighbour joining model was created and visualised.
 - constructor.nj()
 - Phylo.draw()
 - Phylo.draw_ascii()


**THE OUTPUT:**
A neighbour joining phylogenetic tree should be created as a result of running the code.
Details of what the tree should look like is as follows:
- CuAOzeta should be the most divergent from all the other sequences 
- the remaining gene sequences should form 2 clusters/groups:
   - group 1: CuAOepsilon2, CuAOalpha1, CuAOalpha2, CuAOalpha3, and CuAObeta
   - group 2: CuAOdelta, CuAOepsilon1, CuAOgamma1, and CuAOgamma2
 
The output for the phylogenetic tree should look like this:
<img width="281" alt="image" src="https://github.com/KerstinLieu/assessment_dir/assets/153204691/0128df47-4c10-4858-957d-fc705617ddff">


