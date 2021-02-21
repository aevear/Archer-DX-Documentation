# Archer DX Interview Code Documentation

The interview process with Archer DX required that I solve *three* technical problems to measure my skill and coding style.

The problems provided are listed below:

## Problem 1 :

Recursively find all FASTQ files in a directory and report each file name and the percent of sequences in that file that are greater than 30 nucleotides long.

## Problem 2 :

Given a FASTA file with DNA sequences, find 10 most frequent sequences and return the sequence and their counts in the file.

## Problem 3 :

Given a chromosome and coordinates, write a program for looking up its annotation.  Keep in mind you'll be doing this annotation millions of times.

**Input**:
  - Tab-delimited file: Chr<tab>Position
  - GTF formatted file with genome annotations.

**Output**:
  - Annotated file of gene name that input position overlaps.

# Project Notes

I have solved the problem it two seperate ways.

## Solution 1 :

Set in the *basicProject* folder we have three scripts to solve each problem (labeled *Part1*, *Part2* and *Part2* respectively) as well as a results file for part 3 and a sample file containin the information presented from Archer.

This is intended to be the *most direct* and simple solution to the problem, the bare minimum that was asked. There are no external libraries used (aside from default python ones) aside from task three which uses pandas to load and manipulate the data.

## Solution 2 :

As detailed in the *fullProject* folder we have a large scaled version of the project that was turned into a library and simulated what a full project might look like.

### Data
Folder containing *providedData*, *results*, *testData* and *uploadedData*.

- *providedData*: Datasets provided by Archer, used as the default set
- *Results*: the CSV files that store the results of any operation
- *testData*: contains the testing data and testing keys
- *uploadedData*: where data uploaded within the Flask app is stored

### Docs
Contains the documentation information used by *Sphnix* to autogenerate most of the documentation from the source material.

### Flask
The flask component of the project that provides a front end GUI to run all three parts of the code. *Uses a flask template from Appseed*

### Notebook

Where *Jupyter Notebooks* are stored. Currently only contains the optimization notebook used to explore options in part 3.

### Setup.cfg and setup.py
Used to convert this pseudo-library to a local install, allowing it to be called and used in the same way a library is even during development.

### Src
The actual source repository for the code. The rest of the documentation explores this category. There are three main parts

- *main.py* : main entry point for the library, has set options to run parts and provide paths to new data sets.
- *testingMain.py* : main entry point for testing, provides a framework to verify that the code is working as intended during development
- *core* : contains the three problems presented by Archer
- *testing* : the testing code and framework to validate processes are running correctly.
- *utility* : provides support for the rest of the code with *paths* and data *importing and exporting*.
