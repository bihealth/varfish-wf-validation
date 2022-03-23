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

First of all, ensure that `~/.varfishrc.toml` is properly configured, e.g.

```toml
[global]
varfish_server_url = "https://varfish.example.com"
varfish_api_token = "1234567890123456789012345678901234567890123456789012345678901234"
```

Then, copy `config/main.yml.example` to `config/main.yml`.
Adjust the settings:

TODO

## Running

```
# snakemake --configfile=config/main.yml --cores 10 -d workflow
```

