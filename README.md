# Openshift TektonCD operator

This repository holds Openshift's fork of
[`tektoncd/operator`](https://github.com/tektoncd/operator) with additions and
fixes needed only for the OpenShift side of things.

## How this repository works ?

The `master` branch holds up-to-date specific [openshift files](./openshift)
that are necessary for CI setups and maintaining it. This includes:

- Scripts to create a new release branch from `upstream`
- CI setup files
  - tests scripts

Each release branch holds the upstream code for that release and our
openshift's specific files.

## CI Setup

For the CI setup, two repositories are of importance:

- This repository
- [openshift/release](https://github.com/openshift/release) which
  contains the configuration of CI jobs that are run on this
  repository

All of the following is based on OpenShift’s CI operator
configs. General understanding of that mechanism is assumed in the
following documentation.
