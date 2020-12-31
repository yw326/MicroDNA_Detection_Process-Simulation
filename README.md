# Cicular Repeats Postprocessing

## Purpose
This program processes the output from [Circular Repeats Finder](https://github.com/yw326/Circular-Repeat-Finder). More specifically, it removes the overlapping and duplicated data, and provide summary information such as microhomology, GC content and length distribution. 

## Prerequisites

You need to have the output from running the [Circular Repeats Finder](https://github.com/yw326/Circular-Repeat-Finder) (CRF), as well as the DNA sequence file used in CRF.


# Usage

The program takes the following argument
* --seq_path: the path to the DNA sequence file
* --data_path: the path to the circular repeated pairs data. This could be either a file, or a folder containing all the data files.
* --is_data_folder: false if you only want to process a single file. If set to true, circular repeated pairs in all files in the directory speficied by data_path will be aggregated together.
* --output_path: the output folder that will be created to store the summary data and processed circular repeats data.
* --is_direct: set to true if direct circular repeats are processed; otherwise (i.e. when processing inverted circular repeats), set to false

## Example

```
python main.py --seq_path sequence.txt --data_path direct_index.txt --output_path output --is_direct true --is_data_folder false
```

The above command will process all the data in file direct_index.txt and creates a folder named "output" in which processed data are stored.  


## Output Files




