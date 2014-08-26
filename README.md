scapper
=======

Rapid whole genome SNP alignments from multiple draft genomes

Introduction
============

Core genome SNP alignments are useful, but spatial information is lost because converved columns are removed, and non-core regions are excluded. Scapper is a fast way to take a bunch of genomes (closed or draft contigs) and produce a whole genome alignment.

Dependencies
============

* MUMmer >= 3.23  
* BioPerl >= 1.60 
* TrimAL >= 1.4

Installation
============

    % cd $HOME
    % git clone https://github.com/Victorian-Bioinformatics-Consortium/scapper.git
    % $HOME/scapper/bin/scapper -h

Usage
=====

    % ls
    reference.fa draft1.fa draft2.fa draft3.fa
    % scapper --output outname reference.fa draft1.fa draft2.fa draft3.fa
    % ls outname.*
    outname.aln  outname.nogaps.aln  outname.core.aln  outname.nogaps.aln

Output files
============

* `output.aln` has the global alignment with conserved columns and gaps
* `output.nogaps.aln` has the global alignment with all gap columns removed
* `output.core.aln` has the global alignment with conserved columns removed
* `output.nogaps.core.aln` has the global alignment with gaps and conserved columns removed (aka "core SNPs")

Caveats
=======

* Everything is relative to the first genome supplied




