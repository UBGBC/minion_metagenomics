# minion_metagenomics
Nanopore to Bracken Snakemake


Currently Loaded Modules:

`gbc-porechop/0.2.4 python/py37-anaconda-5.3.1 snakemake gcc/11.2.0`

Step-by-step of install and analysis

git clone this repository
git clone https://github.com/UBGBC/minion_metagenomics.git

Activate the python anaconda environment
conda activate snakemake

Edit the config.json file and cluster.json files

Ensure meta-data table contains all of the necessairy fields

** NOTE EXACT HEADERS HAVE TO BE ENFORCED or key errors will be thrown during processing**

Launch jobs
The use of --latency-wait allows for SLURM to catch up writing the files and posting the file handles so Snakemake can see them.

`snakemake --latency-wait 120 -p -j 100 --profile slurm`
