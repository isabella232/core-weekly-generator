# Core Weekly report generator

Core weekly generator is a micro Python 3.4+ CLI application that is able to generate a list of merged PR
for a selected list of branches in an interval of dates.

## Installation

```bash
$ pip install -r requirements.txt
```

## Usage

Display help

```bash
$ ./core-weekly.py --help
usage: core-weekly.py [-h] [--no-cache] [--debug] [--stats] [--year YEAR] date

PrestaShop Core Weekly

positional arguments:
  date         Date range, or week number

optional arguments:
  -h, --help   show this help message and exit
  --no-cache   Disable cache
  --debug      Use Debug
  --stats      Print stats report and save it in json file if you specify a
               week number
  --year YEAR  Specifcy which year you want to use in Week context
  ```

Generate Core Weekly with a date range

```bash
 $ python ./core-weekly.py 2019-08-05..2019-08-11 > my-core-weekly.md
 ```

Or easier by specifing a week number

```bash
 $ python ./core-weekly.py 11 > my-core-weekly.md
 ```

 And if you want the same week but in 2018

```bash
 $ python ./core-weekly.py --year 11 > my-core-weekly.md
 ```

You need to do a bit of polishing (fill in the `[XXXX]` sections, reorder categories, repositories, put the full category names instead of TE or CO) before publishing the article.
