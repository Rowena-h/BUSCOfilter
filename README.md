# BUSCOfilter

A tool to filter [**BUSCO**](https://busco.ezlab.org/) output into folders of common single copy sequences for phylogenetics.

## Requirements

BUSCOfilter is a bash script which runs in the Linux command line. To download, simply use:

```
git clone https://github.com/Rowena-h/BUSCOfilter.git
```

Make the script executable with:

```
chmod +x BUSCOfilter
```

## Usage

Option | Description
------ | -----------
-h, --help | Display these options
-l, --list | A list of assembly names for which busco has been run
-d, --directory | Directory containing busco output folders

If the list of assemblies and number of BUSCO output folders in the provided directory don't match, BUSCOfilter will return an error. To ensure the list matches the BUSCO folders in the directory, and assuming the BUSCO output folders have the typical 'run_' prefix, you can make the list with the following command:

```
ls -d run_* | cut -f 2- -d '_' > assembly_list
```

### Example

```
./BUSCOfilter -l assembly_list -d busco_folders
```
