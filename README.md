# SMU

This repo was forked (not in the git sense of fork, just a copy of the files) from
[https://github.com/google-research/google-research/tree/master/smu]
then modified to be a more standard python package.


This code is for a still in-progress paper and dataset. More details will be
added when the dataset is complete and published.

## Get the data

TODO: once the dataset has been released, include links and md5sums

## Installation instructions (user)

This is probably the process you want. even if you are writing new python code
using the SMU library, you can use this method. It is *only* if you need to modify
the code in the SMU library itself that you need to use the developer mode below

1) Check that you have a compatible version of python
      ```
      python3 --version
      ```
   Should give you a version >=3.6.1.
   If not, you need to upgrade.

1) Go to directory where you want to do the install

1) Create a python virtual environment
      ```
      python3 -m venv smu_venv
      ```

1) Activate the virtual environment
      ```
      source smu_venv/bin/activate
      # Ensure that commands below refer to the virtual enviroment
      rehash
      ```

1) Install the SMU code.
      ```
      # Ensure pip is latest version
      python3 -m pip install --upgrade pip
      # Note that for now we are using test pypi. We'll release to the regular PyPi
      # for final release
      python3 -m pip install --extra-index-url https://test.pypi.org/simple/ smu
      ```

1) Test your installation
      ```
      cd <path where you downloaded the SMU sqlite files>
      python3 -m smu.query_sqlite --input_sqlite 20220621_standard_v4.sqlite --smiles NN
      ```

TODO: Change to the normal PyPi



## Installation instructions (developer)

Are you really sure you need to do this? See previous section.

TODO: write instructions for the new setup

## Next steps

1) [The documentation for smu.query_sqlite](docs/query_sqlite.md) explains
how to use the command line tool to read the SMU database. This is
especially useful to extract small parts of the database, but can also
be used to read the entire thing.

1) [The examples directory](docs/examples.md) gives several example scripts for
accessing the database with python code. Even if you don't plan on
writing python, these examples illustrate some important features of
the data, so it is recommended you read them over.
