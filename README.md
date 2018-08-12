### FOCUS: An Agile Profiler for Metagenomic Data
(c) Silva, G. G. Z., D. A. Cuevas, B. E. Dutilh, and R. A. Edwards, 2014: [FOCUS: an alignment-free model to identify organisms in metagenomes using non-negative least squares. PeerJ.](https://peerj.com/articles/425)


#### (!) IMPORTANT
- If you are using FOCUS cloned from github, please uncompress `db.zip` file inside `focus_app`
- FOCUS  before tool rewrite can be found [here](https://github.com/metageni/FOCUS/archive/0.31.zip)


#### (1) Installation
This will give you command line program:

	# clone focus
	git clone git@github.com:metageni/FOCUS.git

	# unzip database and move it to folder
	unzip FOCUS/focus_app/db.zip && mv db FOCUS/focus_app/

	# install focus
	cd FOCUS && python setup.py install


#### (2) Usage
	focus -q INPUT_DIR -k -o OUTPUT_DIR

		-q Path to directory with FASTA/FASTQ file(s)

		-o Path to output directory

		-k K-mer size (6 or 7 avaliable) (Default: 6)

    	-p Ouput prefix (Default: output)


#### (3) Output
FOCUS generates a tabular output per taxonomic level (`Kingdom`, `Phylum`, `Class`, `Order`, `Family`, `Genus`, `Species`, and `Strain`) and one with all levels which can be used as [STAMP](http://kiwi.cs.dal.ca/Software/STAMP)'s input for statistical analysis.


#### (4) Dependencies
- [Python 3.6](http://www.python.org/download)
- [Setuptools 36.0.1](https://setuptools.readthedocs.io/en/latest/)
- [Jellyfish 2.2.6](https://github.com/gmarcais/Jellyfish/releases/tag/v2.2.6). if using macOS, use [bioconda](https://anaconda.org/bioconda/jellyfish)
- [Numpy](https://github.com/numpy/numpy)
- [SciPy](https://github.com/scipy/scipy)
