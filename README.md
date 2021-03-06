## Overview

pdfmm (for "pdf minus minus", or "pdf--") is a graphical assistant to reduce the size of PDF files.

<img src="https://raw.githubusercontent.com/jpfleury/pdfmm/master/doc/exemple1-en.png" width="683" height="526" alt="Graphical assistant to reduce the size of PDF files" />

Here are some results obtained with PDF files randomly selected:

| Input size | Output size | % optimization |
| ---------- | ----------- | -------------- |
| 29   KiB   | 23   KiB    | 20 %           |
| 363  KiB   | 72   KiB    | 80 %           |
| 733  KiB   | 658  KiB    | 10 %           |
| 991  KiB   | 349  KiB    | 65 %           |
| 1.7  MiB   | 0.8  MiB    | 52 %           |
| 1.9  MiB   | 1.1  MiB    | 40 %           |
| 2.3  MiB   | 1.6  MiB    | 31 %           |
| 3.4  MiB   | 1.3  MiB    | 60 %           |
| 7.1  MiB   | 5.4  MiB    | 23 %           |
| 14.8 MiB   | 9.4  MiB    | 36 %           |
| 54.3 MiB   | 14.6 MiB    | 73 %           |

Of course, this table is presented only as example. The result will certainly not be the same with other files of similar size. It depends on the content.

## Requirements

pdfmm is a shell script requiring bash (>= 4.0), sed, zenity and ghostscript.

## Installation

- [Download the archive of the latest version.](https://github.com/jpfleury/pdfmm/archive/master.zip)

- Extract the archive.

### Current user

The script is ready to be used by the current user.

### All users

To make the script available to all users, add the file `pdfmm` in the folder `/usr/bin/` (root privileges needed).

In this case, the folder created by the extraction can be deleted after the copy.

## Uninstallation

### Current user

Just delete the folder created by the extraction.

### All users

Delete the file `pdfmm` previously copied in `/usr/bin/` (root privileges needed).

## Usage

**Notes:**

- No original files are modified. The optimized file is created in the same folder as the original.

- A configuration file is created in the home folder of the user running `pdfmm`:

		~/.config/pdfmm.conf

	This file contains the parent folder of the last file selected. This folder will be proposed teh next time `pdfmm` will be used.

### Current user

To use the script in a terminal, run the file `pdfmm` with the appropriate access path:

	path/to/pdfmm

If your working folder is the same as the parent of the file `pdfmm`, the command is:

	./pdfmm

In any case, the PDF files to optimize can be specified as an argument, for example:

	./pdfmm path/to/the/file1.pdf path/to/the/file2.pdf

The script can also be opened by clicking on the file `pdfmm` (single click or double click depending on your configuration) and choosing to run it.

If you prefer, you can create a launcher with the absolute path as command, for example:

	/home/USER/path/to/pdfmm

### All users

In a terminal, just enter `pdfmm`. The PDF files to optimize can be specified in command line.

A launcher can also be created with the command `pdfmm`.

## Localisation

pdfmm is translatable. Anyone interested can translate all strings in the section *Localisation* of the file `pdfmm` and send me the result. For now, pdfmm is available in English, in French and in German.

## Development

Git is used for revision control. [Repository can be browsed online or cloned.](https://github.com/jpfleury/pdfmm)

## License

Author: Jean-Philippe Fleury (<http://www.jpfleury.net/en/contact.php>)  
Copyright © 2011 Jean-Philippe Fleury

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
