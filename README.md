# make_subalignment
This script takes a prefix of a subset of (our ingroup) taxa and will return an alignment of only those genes within the clade descended from the most recent common ancestor of all genes with the specified prefix.

## REQUIREMENTS

* There is an embedded python script that requires the dendropy library
 NOTE: There is a $PYTHON3 variable at the top of the script.  The value of this should point to the python3 that has the dendropy library (either a value in the path or the full path)

* JFR::Fasta is required https://github.com/josephryan/JFR-PerlModules

#### usage: ./make_subalignment --tree=<newick_treefile> --aln=<fasta_alignment> --root=<root_taxa> --pre=<prefix> [--phylip] [--help]

### --tree
    input tree in newick format
    
### --root
    outgroup taxon (or comma-separated outgroup taxa)
    
### --aln
    alignment in FASTA format
 
### --pre
    prefix of taxa that make up the ingroup (the last common ancestor of these taxa will make up the ingroup)

### --phylip
    use this flag if input is in phylip format
    
### --version
    print version and exit
    
### --help
    print usage info

## TODO

1. If Inline::Python is installed use it rather than a system call to python

## COPYRIGHT / LICENSE

Copyright (C) 2019 Joseph F. Ryan

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
