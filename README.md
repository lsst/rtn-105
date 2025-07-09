[![Website](https://img.shields.io/badge/rtn--105-lsst.io-brightgreen.svg)](https://rtn-105.lsst.io)
[![CI](https://github.com/lsst/rtn-105/actions/workflows/ci.yaml/badge.svg)](https://github.com/lsst/rtn-105/actions/workflows/ci.yaml)

# Contributing capabilities to the Rubin Science Platform

## RTN-105

The Rubin Science Platform is a coherent ecosystem of integrated services operated (and in most cases developed) by the Data Services division of Rubin Data Management. 

It is possible for second-party (wider Rubin, beyond Data Services) and third-party (external groups) to contribute capabilities for the benefit of all Rubin Science Platform users. 

This document outlines the policies and process for such contributions.

**Links:**

- Publication URL: https://rtn-105.lsst.io
- Alternative editions: https://rtn-105.lsst.io/v
- GitHub repository: https://github.com/lsst/rtn-105
- Build system: https://github.com/lsst/rtn-105/actions/


## Build this technical note

You can clone this repository and build the technote locally if your system has Python 3.11 or later:

```sh
git clone https://github.com/lsst/rtn-105
cd rtn-105
make init
make html
```

Repeat the `make html` command to rebuild the technote after making changes.
If you need to delete any intermediate files for a clean build, run `make clean`.

The built technote is located at `_build/html/index.html`.

## Publishing changes to the web

This technote is published to https://rtn-105.lsst.io whenever you push changes to the `main` branch on GitHub.
When you push changes to a another branch, a preview of the technote is published to https://rtn-105.lsst.io/v.

## Editing this technical note

The main content of this technote is in `index.md` (a Markdown file parsed as [CommonMark/MyST](https://myst-parser.readthedocs.io/en/latest/index.html)).
Metadata and configuration is in the `technote.toml` file.
For guidance on creating content and information about specifying metadata and configuration, see the Documenteer documentation: https://documenteer.lsst.io/technotes.
