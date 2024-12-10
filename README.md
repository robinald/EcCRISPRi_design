All possible sgRNA sequences in the E. coli K-12 MG1655 genome were generated and evaluated as with these scripts.

Briefly, candidate sgRNAs were acquired by dissecting all genic regions into 23 mers that began with the protospacer adjacent motif (PAM) sequence.

These sequences were subjected to a BLASTN-based search for off-target binding as described previously (Sanjana, N.E., Shalem, O., and Zhang, F. (2014). Improved vectors and genome-wide libraries for CRISPR screening. Nature methods 11, 783-784. 10.1038/nmeth.3047).

Sequences that aligned to more than one locus in the genome were excluded.

Then, gRNAs positioned in the CDS were extracted from the CDS list (CDSs extracted from the NC_000913.3 RefSeq annotation) using **Script 1**.

Simultaneously, the CDSs were fragmented every 100 nt (**Script 2**).

The first gRNA in a specific CDS fragment was then selected to make the average distance between the gRNAs 100 nt long.

If certain CDS fragments contained no gRNA, the last gRNA of the previous fragment was selected (**Script 3**).

Finally, the sequences of the selected gRNAs were extracted.
