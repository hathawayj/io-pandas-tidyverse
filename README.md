# Data Science is about communication

This repository houses an invited presentation for Kennesaw State's DS 7900 Applied Project in Analytics and Data Science. 

- [html slides](https://ds7900.github.io/analytics-collaboration-hathaway/#1)
- [pdf slides](https://github.com/DS7900/analytics-collaboration-hathaway/raw/slides/slides.pdf)

## Data parsing example

I use the [marathon data](https://faculty.chicagobooth.edu/george.wu/research/marathon/) that the New York Times article [What Good Marathons and Bad Investments Have in Common] (https://www.nytimes.com/2014/04/23/upshot/what-good-marathons-and-bad-investments-have-in-common.html?rref=upshot&_r=1) used.

They provide links to the entire data of almost ten million records in [csv from box.com](https://uchicago.box.com/s/m6zvhtudswz8mctu1kcxr3a4a33f24qc). I have removed a few columns and provided two formats from dropbox.

- [.sas7bdat](https://www.dropbox.com/s/5h81st5lj0zf85w/marathon.sas7bdat?dl=0) (1.18 Gb)
- [.csv](https://www.dropbox.com/s/pck9qnwmbo4vjsi/marathon.csv?dl=0) (0.566 Gb)

You can find the same data in `.feather` and `.parquet` formats in this repository's `arrow` folder.

### R scripts

- [initial_setup.R](initial_setup.R) provides the script that drops columns from the original source.
- [create_arrow.R](create_arrow.R) provides an example of converting a large file from `.sas7bdat` to `.feather` and `.parquet`. The results are in `arrow`.
- [data_digest.R](data_digest.R) provides size and parsing time for each format.

### Python scripts

- [create_arrow.py](create_arrow.py) provides an example of converting a large file from `.sas7bdat` to `.feather` and `.parquet`. The results are in `py_arrow`
- [data_digest.R](data_digest.py) provides sizes and parsing for `.sas7bdat` and `.parquet`.

## Data exploration example

The [explore_bigdata.R](explore_bigdata.R) file provides a short example.
