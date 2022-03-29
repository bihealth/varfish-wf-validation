# VarFish Workflow: Validation

This Snakemake-based workflow is used for running the validation of VarFish Server.

## Installing

As a prerequisite, install conda and `mamba` package.
Activate `conda`.

```terminal
$ mamba env create -n varfish-wf-validation --file environment.yaml
$ conda activte varfish-wf-validation
```

## Configuring

Copy `config/main.yml.example` to `config/main.yml` and adjust paths.

You will need a number of files for that.

TODO: document how to properly setup

## Running

First, kickoff the import.

```
# cd workflow
workflow # snakemake --cores=10 -p import-started/GRCh37/.done
```

Then, wait until all import jobs have completed.
Future versions will allow you to wait automatically.

Then, kickoff the querying and validation.

```
workflow # snakemake --cores=10 -p validation/GRCh37/all_statuses.txt
```
