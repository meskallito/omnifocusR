# omnifocusR

[![Travis build status](https://travis-ci.org/bkkkk/omnifocusR.svg?branch=master)](https://travis-ci.org/bkkkk/omnifocusR)  [![Codecov test coverage](https://codecov.io/gh/bkkkk/omnifocusR/branch/master/graph/badge.svg)](https://codecov.io/gh/bkkkk/omnifocusR?branch=master)

## Overview

OmniFocus is an excellent task manager application for MacOS and iOS by the folks at [OmniGroup](https://www.omnigroup.com), it is based on the ideas of Getting Things Done, but supports other methodologies as well.

omnifocusR converts your OmniFocus data into a convenient tidy data frame ready for analysis.

omnifocusR is partially compatible with OmniFocus 3, primarily missing is multi-tagged task support.

## Installation

```r
# install.packages("devtools")
devtools::install_github("bkkkk/omnifocusR")
```

## Usage

To use omnifocusR you first need to export your database:

1. In OmniFocus, go to *File -> Export...*
2. Select *OmniFocus document* as the File Format
3. Right-click on the newly exported `ofocus` package and select *Show Package Contents*
4. Unzip the file to any location
5. You will note that a single XML file called *contents.xml* was extracted
6. In R:

```r
# library("omnifocusR")
tasks <- process_of_db("PATH_TO_CONTENTS.XML_FILE")
```

This will return a data frame (wrapped as a *tbl_df*) that contains all the tasks in the ofocus file with context and project names.

----

## Disclaimer

This project and it's contributors are not related in any way, shape or form to the OmniGroup or any organization related to them. This package was not built, tested, sanctioned, blessed, approved by the OmniGroup, nor is it maintained by them. They probably haven't got a clue that it exists. If something breaks because you used it, it's on you. I make no claims to OmniFocus or any of the OmniGroup applications, they are awesome and you should use them.
