# Bandcamp import

This script is an helper to reformat the bandcamp archives to the way I organized music.

## Installation

Just install and activate the conda environment:

```sh
conda env create -f environment.yml
conda activate bandcamp
```

## Run

The command is the following:

```sh
usage: generate.py [-h] [-l LOG_FILE] [-s SEPARATOR] [-v]
                   input_csv input_dir output_dir

positional arguments:
  input_csv             The CSV file which contains the meta-information
  input_dir             The directory containing the zip files downloaded from
                        bandcamp
  output_dir            The root directory which will contain the music
                        unpacked and organized

optional arguments:
  -h, --help            show this help message and exit
  -l LOG_FILE, --log_file LOG_FILE
                        Logger file
  -s SEPARATOR, --separator SEPARATOR
  -v, --verbosity       increase output verbosity
```

The input CSV fileshould contain the following information:
 - **Artist:** The name of the artist
 - **Album:** The album name
 - **Year:** The release year of the album

The separator is user defined via the option `-s`. The default value is `\t`
