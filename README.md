# BUSCOfilter

A tool to filter [**BUSCO**](https://busco.ezlab.org/) output into files of single copy-sequences to be aligned for phylogenomics.

<img src="schematic.PNG" width="500">

## Requirements

BUSCOfilter is a bash executable which runs in the Linux command line. The current version is up to date for BUSCO v5.7.1 output. Download the [latest release](), or use:

```
git clone https://github.com/Rowena-h/BUSCOfilter.git
```

## Usage

Option | Description
--------- | -----------
-h, --help | Display these options
-d, --directory | Directory containing BUSCO (>= v5.7.1) output folders which contain subdirectories with the typical `run_` prefix.
-m, --mode | Set whether to produce files for all single-copy BUSCOs in the genomes or only those with a BUSCO in all genomes. Options `all` or `common` [Default = `common`]


### Example

```
./BUSCOfilter -d /data/busco_folders -m all
```

## Output

In addition to a folder containing fasta files for each selected single copy BUSCO, the following files are produced when running BUSCOfilter:

File | Description
------ | -----------
assembly_list | A list of the genomes found in the provided directory (i.e. the name of each BUSCO output folder after the 'run_' prefix).
busco_stats | A tabular summary of the BUSCO run statistics for all the provided genomes.
busco_list | A list of IDs for the single copy BUSCOs that files were made for. If using `-m all` this will have a second column with the number of genomes that each BUSCO was found in.
error_list | If any of the BUSCO fasta files have the incorrect number of sequences when using `-m common`, the BUSCO IDs are stored in this file so that fasta files can be manually checked.

## Citation

If you use BUSCOfilter in your work please cite:
> Hill R. (2024) BUSCOfilter. https://github.com/Rowena-h/BUSCOfilter