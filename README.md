# FASTA
A Python command-line tool that parses DNA sequences in FASTA format, translates codons into amino acids, and classifies point mutations as Silent, Missense, or Nonsense. Built independently as part of a self-directed bioinformatics project during the first year of a B.Tech Biotechnology program at VIT.
What It Does
Given a reference and a mutant DNA sequence (in FASTA format), the tool:

Parses and cleans both sequences
Translates each codon using a full codon table
Identifies every position where the sequences differ
Classifies each mutation by its effect on the protein:

Silent — DNA changes, amino acid stays the same
Missense — DNA changes, amino acid changes
Nonsense — DNA change introduces a premature STOP codon
Example Output
Tested on the human insulin gene (INS) with an introduced nonsense mutation at position 181 (TAC → TAG):
Pos    | DNA Chg    | Type         | AA Change
-------------------------------------------------------
181    | C -> G     | NONSENSE     | Y -> STOP

--- Protein Result ---
Ref: M-A-L-W-M-R-L-L-P-L-L-A-L-L-A-L-W-G-P-D...
Mut: M-A-L-W-M-R-L-L-P-L-L-A-L-L-A-L-W-G-P-D...
