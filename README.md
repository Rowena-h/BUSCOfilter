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
-d, --directory | Directory containing busco output folders which must have the typical 'run_' prefix


### Example

```
./BUSCOfilter -d /data/busco_folders
```
