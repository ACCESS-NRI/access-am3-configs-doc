
# Home

!!! warning
    This model uses components and science configurations from the UK Met Office (UKMO), and as such are license restricted. This means the associated repositories are required to be private. If you would like to be granted access to these repositories, please get in touch **where?**.

Welcome to the documentation for the [ACCESS-AM3 model configurations](https://github.com/ACCESS-NRI/access-am3-configs)! 

!!! warning
    This documentation is still under construction. It will be improved during the alpha testing. We welcome any [contributions](/contributing).

## ACCESS-AM3 Documentation Overview

The documentation in split into 4 main sections, which also have navigation links in the left sidebar:

 - [Contributing](/contributing) 
 - [Inputs](/inputs/Forcing-data-models) 
 - [Configuration choices/Configurations](/configurations/Overview/) 
 - [Infrastructure](/infrastructure/Architecture/) 

## access-am3-configs Overview
ACCESS-AM3 configurations are provided via branches in the [access-am3-configs](https://github.com/ACCESS-NRI/access-am3-configs) GitHub repository, this repository is currently private. The [access-am3-configs](https://github.com/ACCESS-NRI/access-am3-configs) repository contains several configurations using the following components:

- [UM](https://github.com/ACCESS-NRI/UM) atmosphere model
- [CABLE](https://github.com/CABLE-LSM/CABLE) land model
- [JULES](https://github.com/ACCESS-NRI/JULES) land model

All the configurations use the [_Rose/Cylc_ workflow management tools](https://docs.access-hive.org.au/models/run_a_model/rose_cylc/), and pre-built executables available on [NCI](https://nci.org.au/).

### Repository structure

Each configuration in [github.com/ACCESS-NRI/access-am3-configs](https://github.com/ACCESS-NRI/access-am3-configs) repository is stored as a git branch. Most of the branches are named according to the following naming scheme:

* {dev|release}-{nominal_resolution}

where {nominal_resolution} is the spectral resolution following the conventions from the UK Met Office (UKMO).

#### Supported configurations

* N96e global coupled atmosphere-land.

#### How to use this repository to run a model

All configurations use [_Rose/Cylc_](https://docs.access-hive.org.au/models/run_a_model/rose_cylc/) to run the model.

This repository contains many related experimental configurations to make support
and discovery easier. As a user it does not necessarily make sense to clone all the
configurations at once.

In most cases only a single experiment is required. If that is the case, choose which experiment and then run

```sh
git clone -b <experiment> https://github.com/ACCESS-NRI/access-am3-configs <experiment>
```

and replace `<experiment>` with the branch name or tag of the experiment you wish to run.

[ACCESS-Hive](https://access-hive.org.au/) contains [detailed instructions for how to configure and run ACCESS models with `payu`](https://access-hive.org.au/models/run_a_model).

#### CI and Reproducibility Checks

This repository will make use of GitHub Actions to perform reproducibility checks on model config branches.
