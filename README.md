# Repro for pre-commit-hooks issue, #781

## Introduction

This repo contains files necessary to easily reproduce
[#781](https://github.com/pre-commit/pre-commit-hooks/issues/781).

## Steps to Reproduce

From the working directory:

```sh
pre-commit run --all-files
```

## Expected Result

_my-binary-file_ remains unchanged because it is attributed binary in _.gitattributes_.

## Actual Result

A byte, value 10, is appended to _my-binary-file_ as if it were an LF-delimited text file.
