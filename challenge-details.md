## CHALLENGE DATA

The data set for this challenge is a 330MB raw file. It has no file system, but it contains many files and file fragments. The file types used in the DFRWS 2006 carving challenge may be in this challenge (JPEG, ZIP, HTML, Text, and Microsoft Office) and this year adds more multimedia, document, and e-mail formats. Example new formats include, but not limited to, MP3, MPG, WMV, PDF, and executables.

All files in the image are distributed using their original copyrights. Specific attribution and copyright details will be released after the challenge is over. All files are either public domain or have a license that allows for non-commercial distribution.

Before you begin recovering data, you should review the DFRWS submission format requirements (listed below).

File image (300 Mb Zip): [dfrws-2007-challenge.zip](https://www.dropbox.com/s/5ze0r2o1vjxf811/dfrws-2007-challenge.zip?dl=0)

MD5 of raw file: 8a501f3f525c85a50a3aa0bf698bffe7

Note that some of the files in this image were released on the Internet with license restrictions. Refer here for details.

## ALLOWED ANALYSIS TECHNIQUES
The data should be analyzed using little or no human intervention. We respect attempts to recover data manually, but that does not typically scale with realistic data sizes and therefore findings that rely on human intervention will be given less weight than findings that are obtained in an entirely automated manner. As with last year, the source code for the tools developed for the submission must be released (under any restrictions and license that you choose).

This year, we will also not accept submissions that manually use data from the Internet to find a full file from a fragment. For example, finding a fragment in the challenge data, manually searching the Internet for the full file, and then finding the remaining file fragments in the disk image. Techniques that use the Internet in an entirely automated fashion for recovery may be considered. For example, an automated technique may, without human intervention, find a file fragment in the data, search the Internet for the fragment, and then search the data for the remaining fragments.

## SUBMISSION REQUIREMENTS

### Reporting Format:

To make grading easier, all submissions must be in a common format. Provide the following data in a table layout like the one below:
- MD5 hash
- Sectors from where the file was carved (assume 512-byte sectors). Use a dash to denote a range of sectors and a comma in between fragments. For example, if the file as found in sectors 3, 4, 5, 6, and 10 then document this as "3-6,10".
- File size (in bytes)
- File type (JPG, ZIP, MP3, etc.)

The table layout must have the columns in this order:
```
MD5                              | Sectors | File Size | File Type
38ac5491aabfb73efdf62cbe8e866d28 | 3-6,10  | 2413      | JPG
```

### False Positives
We will be calculating the false positive rates for submissions and therefore we recommend that you organize your files into two categories: ones that were completely recovered (i.e. the recovered file is identical to the original) and ones that have missing fragments. We will primarily focus on the files that were completely recovered, but the partially recovered files will also be considered in cases of ties or if a novel algorithm was used to find the fragments. If you do not separate the completely and partially recovered files, then the partially recovered files will be added to your false positive rate. Ideally, your recovery tools will be able to separate the files into the different categories.

Files that are not completely recovered must be able to be opened using standard viewing programs. For example, a partially recovered JPEG file should be able to be viewed using standard programs even though some of the picture may be blank since the fragment is missing. You are allowed to use automated techniques to add standard headers and other data structures to files where fragments are missing. For example, you could add a JPEG header to a fragment if the header was missing. If you do this, you must submit the resulting file and describe the technique used.

### Source Code
The goal of this challenge is to advance the state of the art in research and tools. Therefore, we require that you document your techniques as much as possible. Publishing source code for the tools developed is the preferred method for doing this (the code can be released under any restrictions and license that you choose). This year, we are also allowing submissions to document the algorithms and techniques using some form of pseudo-code as long as they also submit an executable that implements the technique (the executable will not be published with the submission). The pseudo-code must be detailed enough such that someone else could implement the approach and obtain the same results. As with automation, submissions that include source code will be graded higher than submissions that include pseudo-code. Submissions with pseudo-code that does not adequately describe the process will not be considered in the final grading.

### Report Contents

The submission must describe how the files were extracted and tested. For accurate evaluation, make these answers easy to find (i.e. you could have a section for each of them). This includes:
- The name and version of existing carving programs that were used.
- A description of algorithms you developed for the challenge.
- Working source code of tools you developed for the challenge or pseudo code and a working executable (the executable will not be published with the submission on the website).
- How the number of false positives was reduced.

Further details about the challenge data are available, with which you should familiarize yourself before beginning to recover the data.
