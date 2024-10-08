# Auto1 ETL Challenge

A simple ETL pipepline that serves the purpose of a challenge for [AUTO1](https://www.auto1.com/en/home), a company that is Europe's largest wholesale platform for used cars.

Developed by Muhammad Aqib - inbox.aqib@gmail.com

# Contents

- `auto1_etl_challenge` contains the project directory.
- `auto1_etl_challenge\etl.py` is the main module that has `EtlPackageAuto1` class with associated methods.
- `auto1_etl_challenge\utils.py` holds utilites that assists in performing etl operations.
- `auto1_etl_challenge\transformations.py` module for defining custom exceptions for the required columns.
- `auto1_etl_challenge\constants.py` holds classes for different constant values.
- `files` is a directory for storing files for testing purpose, specifically raw, staging and transformed files.

# How To Use

### Package Installation

[auto1-etl-challenge](https://pypi.org/project/auto1-etl-challenge/)

Install the package in the virtual environment

```sh
pip install auto1-etl-challenge
```

### Code Guidelines

- Create a python file and import `EtlPackageAuto1` class from the package.
- Provide source file path in the constructor.
- Call `load` and `transform` method.

```python
from auto1_etl_challenge import EtlPackageAuto1 #import EtlPackageAuto1 class form package

EtlPackageAuto1(r'files\challenge_me.txt') #stores path of the source file
EtlPackageAuto1.load(EtlPackageAuto1.dataFile) # loads data and create staging file with cleaned data
result = EtlPackageAuto1.transform(EtlPackageAuto1.dataFile) # transform data, create transformed file and return list matrix
```

### Output

- Staging and transformed files are created in the same directory as source file.
- List of lists is returned where first list is header while the following lists contain the values (row-wise).


[Github](https://github.com/muhammad-aqib/auto1_etl_challenge)