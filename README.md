# Counting de

> Counting the article 'de' in the [Wikipedia article of the RUG](https://nl.wikipedia.org/wiki/Rijksuniversiteit_Groningen).

## Quick start

- Use the `./download` script to download the current version of the [Wikipedia article of the RUG](https://nl.wikipedia.org/wiki/Rijksuniversiteit_Groningen).
- Use the `./count_de` script to count the occurrences of the dutch article 'de' in 
  the downloaded file.

Note: see bellow for more detailed instructions.

## Installation 

Clone this repository and change directory into it:
```console
$ git clone git@github.com:twanh/IRM_wk5-RUG-wiki && cd IRM_wk5-RUG-wiki
```

Make the `download` and `count_de` scripts executable.
```console
$ chmod +x download
$ chmod +x count_de
```

## Usage

If you have completed the installation process you can now use both the `download` 
and `count_de` scripts to get the data and count the occurrences of 'de'.

### Getting the input data

Using the `download` script the input data can be downloaded.
It automatically downloads the text contents of the [Wikipedia article of the RUG](https://nl.wikipedia.org/wiki/Rijksuniversiteit_Groningen).

Note that this repository currently has one data file pre downloaded (`wikipedia_rug_15_03_2022.txt`)
and it's information is available in the [current collected data](#current-collected-data) section.

#### Usage of `./download`

```
$ ./download [filename]
``` 

The `filename` option can be used to save the file to a custom location.
If no `filename` is given the output is saved to `wikipedia_rug_[current date].txt`
where `[current date]` is the current date (formatted as: `dd_mm_yyyy`).

#### Example without `filename`  

```console
$ ./download
Downloading wikipedia page for the Rijksuniversiteit Groningen
using url: https://nl.wikipedia.org/w/index.php?title=Rijksuniversiteit_Groningen&action=raw
Downloaded the wikipedia page, saved as wikipedia_rug_15_03_2022.txt
```

#### Example with `filename`

```console
$ ./download wiki_rug.txt
Downloading wikipedia page for the Rijksuniversiteit Groningen
using url: https://nl.wikipedia.org/w/index.php?title=Rijksuniversiteit_Groningen&action=raw
Downloaded the wikipedia page, saved as wiki_rug.txt
```

### Counting the article 'de'

Using the `count_de` script the word 'de' can be counted in a text file, and more
specifically in the downloaded data files.

#### Usage of `./count_de`

```
$ ./count_de [filename]
```

The `filename` option can be used to count the occurrences of 'de' in a specific
(text) file.

If the `filename` option is left blank or is not a file, the script looks
for all files starting with `wikipedia_rug_` and uses the file with the most
recent date suffix to count the word 'de' in.


#### Example without `filename`

```console
$ ./count_de
Count of 'de' (case insensitive) in wikipedia_rug_15_03_2022.txt:
251
Count of 'de' (case sensitive) in wikipedia_rug_15_03_2022.txt:
217
```

#### Example `filename`

Note: the `example.txt` file is just to demonstrate the idea and does not
exist within this repository.

```console
$ ./count_de example.txt
Count of 'de' (case insensitive) in example.txt:
251
Count of 'de' (case sensitive) in example.txt:
217
```

## Current collected data

| filename                       | date       | # 'de' (case insensitive) | # 'de' (case sensitive) |
|--------------------------------|------------|---------------------------|-------------------------|
| `wikipedia_rug_15_03_2022.txt` | 15-03-2022 | 251                       | 217                     |

## Versions

The versions of important software used:

- OS: `Ubuntu 20.04.3 LTS x86_64`
- Kernel: `5.13.0.-30-generic`
- Bash version: `GNU bash, version 5.0.17(1)-release (x86_64-pc-linux-gnu)`
- Default shell: `zsh`, with version `zsh 5.8 (x86_64-ubuntu-linux-gnu)`

 



