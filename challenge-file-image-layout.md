## OVERVIEW

The DFRWS 2007 Challenge file contained 85 complete files (not including the embedded files, such as pictures in Word documents or the files inside of ZIP files) and numerous other files that were incomplete and missing fragments. The files were used to create 89 different scenarios, which are described in the next section. Each scenario was designed to test a specific situation that might occur in a real file system. Existing tools can handle only the most basic scenarios in this challenge.

The image file was created using a program that was configured based on the 89 scenarios. The distance between the fragments in a scenario and between the scenarios was random and the data in between fragments filled with either random data or small fragments of other files. The files came from either our own collections or from the Internet. Where needed, we have given credit to the corresponding files from the Internet.

## SCENARIOS
The scenarios used for the challenge were organized into four levels, based on the difficulty of recovering the files. Each level has different scenarios based on number of fragments and file types. Each scenario was given a unique id.

### Level 0: Non-fragmented files:

Scenario     |   Description
| --- | --- |
1            |   Office
2            |   JPG
3            |   ZIP
4            |   MP3
5            |   MP4
6            |   AVI
7            |   MOV
8            |   FLV
9            |   MBOX
10           |   EXEC
11           |   PDF
12           |   MPG

### Level 1: Fragments in sequential order:

Scenario     |   Description
| --- | --- |
14           |   1 Office with filler in between
15           |   1 JPG with filler in between
16           |   3 JPG files intertwined
17           |   4 JPG files intertwined
18           |   1 ZIP with filler (2, 1)
19           |   1 MP3 with filler in between
20           |   2 MP3 files intertwined
21           |   4 MP3 files intertwined
22           |   1 MP4 with filler in between
23           |   2 MP4 files intertwined
24           |   1 AVI with filler in between
25           |   1 MOV with filler in between
26           |   3 MOV files intertwined
27           |   1 FLV with filler in between
28           |   1 MBOX with MBOX in between
29           |   2 MBOX files intertwined
30           |   3 MBOX files intertwined
31           |   1 EXEC with filler in between
32           |   2 EXEC files intertwined
33           |   1 PDF with filler in between
34           |   2 PDF files intertwined
35           |   1 MPG with filler in between
36           |   2 MPG files intertwined
37           |   1 WMV with filler in between
89           |   1 PDF with MBOX in between


### Level 2: Fragments in non-sequential order:

Scenario |	Description
| --- | --- |
38           |   1 JPG 2 frags (2, 1)
39           |   1 JPG 3 frags (3, 1, 2)
40           |   1 JPG 3 frags (3, 2, 1)
41           |   1 JPG 3 frags (1, 3, 2)
42           |   1 JPG 4 frags (1, 3, 2, 4)
43           |   1 Office 2 frags (2, 1)
44           |   1 Office 3 frags (2, 1, 3)
45           |   1 MBOX 2 frags (2, 1)
46           |   1 MBOX 3 frags (3, 2, 1)
47           |   1 MBOX 3 frags (1, 3, 2)
48           |   1 MP3 2 frags (2, 1)
49           |   1 MP3 3 frags (1, 3, 2)
50           |   2 MP3 2 frags (1b, 2b, 1a, 2a)
51           |   1 PDF 2 frags (2, 1)
52           |   1 PDF 3 frags (2, 3, 1)
53           |   1 MPG 2 frags (2, 1)
54           |   1 MPG 3 frags (3, 2, 1)
55           |   1 MOV 2 frags (2, 1)
56           |   1 EXEC 2 frags (2, 1)
57           |   1 EXEC 3 frags (2, 1, 3)


### Level 3: Files with missing fragments:

Scenario     |   Description
| --- | --- |
58           |   1 Office 2 frags, missing end (1)
59           |   1 Office 3 frags, missing middle (1, 3)
60           |   1 JPG 2 frags, missing end (1)
61           |   1 JPG 3 frags, missing middle (1, 3)
62           |   1 JPG 3 frags, missing end (1, 2)
63           |   1 JPG 3 frags, missing middle, last first (3, 1)
64           |   1 MP3 2 frags, missing end (1)
65           |   1 MP3 3 frags, missing end (1, 2)
66           |   1 MP3 3 frags, missing middle (1, 3)
67           |   1 MP3 3 frags, missing end, middle first (2, 1)
68           |   2 MP3 2 frags intertwined, 2nd missing end (1a, 2a, 1b)
69           |   2 MP3 2 frags, 1st missing end, 2nd missing start, continuous (1a, 2b)
70           |   2 MP3 2 frags, 1st missing end, 2nd missing start, filler in between (1a, FILLER, 2b)
71           |   2 MP3 2 frags, 1st missing end, 2nd out of order(1a, 2b, 2a)
72           |   2 MP3 2 frags, 2nd missing start and in between 1st frags (1a, 2b, 1b)
73           |   1 MP4 2 frags, missing end (1)
74           |   1 MOV 2 frags, missing end (1)
75           |   1 MBOX 2 frags, missing end (1)
76           |   1 EXEC 2 frags, missing end (1)
77           |   1 PDF 2 frags, missing end (1)
78           |   1 PDF 3 frags, missing middle (1, 3)
79           |   1 PDF 3 frags, missing end (1, 2)
80           |   1 PDF 3 frags, missing end, 2nd first (2, 1)
81           |   1 MPG 2 frags, missing end (1)
82           |   1 MPG 3 frags, missing end (1, 2)
83           |   1 MPG 3 frags, missing middle (1, 3)
84           |   2 MPG 2 files, 1st missing end (1a, 2a, FILLER, 2b)
85           |   2 PDF 2 files, 1st missing end (1a, 2a, FILLER, 2b)
86           |   2 EXEC 2 files, 1st missing end (1a, 2a, FILLER, 2b)
87           |   2 MP4 2 frags, 1st missing end (1a, 2a, FILLER, 2b)
88           |   MP4 and MOV, 1st missing end, 2nd missing start (MP4a, MOVb)

## IMAGE FILE LAYOUT
Based on the scenarios described in the previous section, a layout of files was created. The layout can be found in the comma delimited file ([dfrws2007-challenge-layout.txt](dfrws2007-challenge-layout.txt)) in the DFRWS 2007 Challenge repository. Each row describes a file fragment and its location. The following columns are used in the layout file:

- Name: File name of fragment
- Type: Type of file
- FileIdx: The index of this file fragment (starting at 0)
- FileSectorOffset: The range of 512-byte sectors of this fragment in the original file.
- ImageSectorOffset: The range of 512-byte sectors of this fragment in the image file. "not used" means that the fragment was not included in the image file.
- Scenario: Id of the scenario the fragment was used in.

## INDIVIDUAL FILE INFORMATION

The csv text file [dfrws-challenge-file-info.txt](dfrws-challenge-file-info.txt) contains information on each file in the challenge. Each entry lists the original file name, MD5, and size. Many of the files were in the public domain, but some require attribution. Those are listed in the file [dfrws-2007-challenge-attribution.html](dfrws-2007-challenge-attribution.html).
