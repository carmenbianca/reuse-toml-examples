<!--
SPDX-FileCopyrightText: 2023 Carmen Bianca BAKKER <carmenbianca@fsfe.org>

SPDX-License-Identifier: CC0-1.0
-->

# REUSE.toml examples

This repository is one big example of how REUSE.toml usage might work. Consider
each subdirectory to be its own 'repository'.

You may wish to use `reuse lint --json` to more closely inspect the tool's
findings.

## 3rd-party

This directory demonstrates how to declare the licensing of 3rd-party vendored
code (static dependencies). You don't normally want to manually edit the files
in vendored code; just paste them and use them.

## glob-directory

Glob the contents of a directory (and only that directory; not its
subdirectories.)

## img-glob

This directory demonstrates a simple glob on an image directory.

## match-file

If a file is in REUSE.toml's 'path' key without directory separators ('/'), then
any file named as such matches.

The rationale for this is mostly that globs like `*.py` work in this way,
instead of having to do something like `**/*.py` or `**.py`. This closely
resembles (but does not precisely match) the way that `.gitignore` patterns
work.
