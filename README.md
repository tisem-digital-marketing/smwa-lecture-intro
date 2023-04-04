# Social Media and Web Analytics: Course Intro

[![lifecycle](https://img.shields.io/badge/lifecycle-maturing-blue.svg)](https://www.tidyverse.org/lifecycle/#maturing)
[![lifecycle](https://img.shields.io/badge/version-2022-red.svg)]()

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />

## Meta-Information

* Module Maintainer: Lachlan Deer (`@lachlandeer`)
* Course: [Social Media and Web Analytics](https://tisem-digital-marketing.github.io/2023-smwa)
* Institute: Dept of Marketing, Tilburg University
* Current Version: [Spring 2023 edition](https://tisem-digital-marketing.github.io/2023-smwa)

## Introduction

Slides for the Course Introduction of Social Media and Web Analytics

Slides are a xaringan presentation and are built to html and pdf using the Snakemake workflow management system.
I also manage R's package dependencies with `renv`.

## How to Build the Slides:

1. Install R, Snakemake and xaringan (see below).
2. Navigate to this project's directory and then run: `snakemake all --cores 1`
   * End result is a html and pdf presentation

## Installation Instructions

Follow these Steps to install the necessary software on your system

You need to have the following software and packages installed:

1. Python 3 (Python 3.6 or higher)
2. Snakemake (we'll install it in a couple of lines time!)
3. R (version 4.0.x)

### Installing Python

Either:

1. Install Anaconda Python:
    - We provide instructions on how to install anaconda python [here](https://pp4rs.github.io/2020-uzh-installation-guide/python/)
2. Install Python using the deadsnakes ppa (Debian/Ubuntu flavored):
    - Here's how to add the deadsnakes ppa and install Python 3.8
    ```bash
    $ sudo apt-get install software-properties-common
    $ sudo add-apt-repository ppa:deadsnakes/ppa
    $ sudo apt-get update
    $ sudo apt-get install python3.8
    ```

### Installing Snakemake

I have included a `requirements.txt` file that we can use to install a specific version of snakemake.
This makes sure that my example runs on your machine (or at least won't break because you use a different version of snakemake than I do)

``` bash
pip3 install -r requirements.txt
```

you may need to replace `pip3` with `pip`

### Installing `R`

We provide instructions on how to install R [here](https://pp4rs.github.io/2020-uzh-installation-guide/r)

### Installing `xaringan`

Either:

1. Install it using `install.packages('xaringan')` in the R console

2. Use our renv workflow:

Open a terminal and navigate to this directory.
Then in the terminal enter the following command to install renv:

``` bash
snakemake --cores 1 renv_install
```

Then you will need to provide consent for `renv` to be able to write files to your system:

``` bash
snakemake --cores 1 renv_consent
```

Once this is complete you can use renv to create a separate R environment that contains the packages we use in our example by entering the following command into the terminal:

``` bash
snakemake --cores 1 renv_init
```

The above command will initialize a separate R environment for this project.

Now we will install the necessary packages (and their precise versions) which are stored in the `renv.lock` file:

``` bash
snakemake --cores 1 renv_restore
```

This will install all the packages we need. It may take a while.

## Suggested Citation

Deer, Lachlan. 2023. Social Media and Web Analytics: Course Introduction.
Tilburg University.
url = "https://github.com/tisem-digital-marketing/smwa-lecture-intro"

```
@misc{smwa2023_intro,
      title={"Social Media and Web Analytics: Course Introduction"},
      author={Lachlan Deer},
      year={2023},
      url = "https://tisem-digital-marketing.github.io/2023-smwa"
}
```
