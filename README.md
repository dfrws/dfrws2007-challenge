# dfrws2007-challenge
DFRWS 2007 Challenge Overview

The DFRWS 2007 Challenge is an international competition to advance the state-of-the-art of data carving, which is a file recovery technique that is frequently used during digital investigations. Files are "carved" from the unallocated space using file type-specific information, such as footers, headers, and internal structures.

The results of existing file carving tools typically contain many false positives and fail to recover some files. An investigator must test each of the extracted files by opening them in an application that supports the file type. The goal of this challenge is to design and develop automated file carving algorithms that identify more files and reduce the number of false positives.

The previous DFRWS 2006 Challenge focused on carving basic file types in basic scenarios. The result was the development of new tools and techniques to carve files using more internal structure than only the header and footer values. The DFRWS 2007 Challenge introduced more file types and more complex fragmentation scenarios.

Further details about the challenge data are available, with which you should familiarize yourself before beginning to recover the data.

## Winner

[Michael Cohen](challenge-submissions/michael.cohen) based his work on a theory of fragmentation and file mapping, and developed dedicated validators for PDF, ZIP, MIME, HTML and MPEG. His process involved evaluating possible files against an ideal mapping model, performing interpolation when discontinuities were found, and then performing error checking on the resulting files using his validation utilities. Even though Cohen did not focus on image and office file formats, his results still ended up very high, with the lowest false positive score. The high quality of the results from this approach shows promise.

## CHALLENGE ORGANIZERS

- Brian Carrier
- Eoghan Casey
- Wietse Venema
