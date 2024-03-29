# DFRWS 2007 Challenge Results

There were five submissions to the DFRWS 2007 Forensics Challenge. As can be seen from the layout, this challenge was much more difficult than the 2006 challenge and we received feedback at the DFRWS 2007 conference that many did not even attempt this challenge because it seemed too daunting! So, we applaud the efforts of those who submitted their results.

Many of the scenarios in the challenge involved fragmented files where fragments were sequential, out of order, or missing. Existing tools could not handle these scenarios and new techniques had to be developed.

We thank everyone for the time they spent on this challenge and their willingness to share their results and techniques with the community.


## THE RESULTS

First Place: Michael Cohen

Second Place: Omar Al-Dahir, Joseph Hua, Lodovico Marziale, Jaime Nino, Golden G. Richard III, and Vassil Roussev

Third Place: Kristofer Munsterhjelm

Fourth Place: Joachim Metz, Bas Kloet, and Robert-Jan Mora

Fifth Place: Christophe Grenier


## SUMMARY OF SUBMISSIONS

[Cohen](challenge-submissions/michael.cohen) based his work on a theory of fragmentation and file mapping, and developed dedicated validators for PDF, ZIP, MIME, HTML and MPEG. His process involved evaluating possible files against an ideal mapping model, performing interpolation when discontinuities were found, and then performing error checking on the resulting files using his validation utilities. Even though Cohen did not focus on image and office file formats, his results still ended up very high, with the lowest false positive score. The high quality of the results from this approach shows promise.

[Al-Dahir, Hua, Marziale, Nino, Richard, and Roussev](challenge-submissions/golden.richard/dfrws2007-UNO.zip) developed several new tools for specific file types, using known characteristics about the formats to locate and combine fragments. In particular, the structure-based tool for mp3 files scored better than the other submissions. The structure-based tools for mail, avi and Zip files fared less well, but show promise. Although their total result was strong, they had a larger number of false positives. This is a very promising approach to structured data.

[Munsterhjelm](challenge-submissions/submit2007-minusextractedfiles.zip) used a combination of techniques: puzzle solving for some structured file types, n-gram for unstructured files, a Rabin-Karp (i.e. sliding) hash for email header signature detection, and naive carving and external validators for other file types. All the PDF files were found with a tool that scans the image for PDF \Title headers and then searches the web. In fact, this is the only way that fragmented files were recovered. Although the results were not strong, the combination of techniques was innovative.

[Metz, Kloet, and Mora](challenge-submissions/joachim.metz) used an approach they call "smart carving," which combines file structure details, content analysis, and block-based carving as part of a linear process, followed by an iterative post-carving validation/analysis process (e.g., spectral analysis of image files, data similarity/dissimilarity analysis). This approach did not work well with fragmented files and was ineffective against out-of-order fragmentation. Their use of generic validators limited accuracy.

[Grenier's TestDisk](challenge-submissions/christophe.grenier/dfrws-2007-grenier.tar.bz2) got more of the unfragmented files than anyone else, but none of the fragmented ones.


## JUDGING PROCESS

For a file to count as recovered, we required either a matching MD5 hash or a matching complete set of block ranges. This allowed for the existence of file types without distinct end markers, and for other ambiguities in the implementation of file formats.

To award the development of new techniques we awarded scores that varied with scenario complexity. The simplest, unfragmented, scenarios were given a weight of one. Fragmented scenarios counted as two, and out-of-order fragmented scenarios counted as three.

When two submissions received similar scores, we gave preference to the one with fewer false positives, that is, files reported as recovered that did not match an MD5 hash or a complete set of block ranges.

The highest scores were awarded to the submissions that were considered most successful with the recovery of files from their out-of-order fragments. The lowest scores were awarded to the submissions that got most or all of their points from the recovery of unfragmented files.

