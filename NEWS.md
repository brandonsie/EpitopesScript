
# epitopefindr 1.1.30 (2020-09-19)
## Minor changes
- Keep blast alignment table as data.table::data.table to fix changes in R 4.0
- changed pdf merge default to pdfuniter to get around rJava issue

# epitopefindr 1.1.29 (2020-05-30)
## Minor changes
- Specify remote sources for Bioconductor and Github package dependencies.

# epitopefindr 1.1.28 (2020-05-07)
## Minor changes
- multiple sequence alignment consensus sequence defaults changed. Consensus sequence type = "upperlower", thresh = c(100, 50). See ?msa::msaConsensusSequence for more information.

# epitopefindr 1.1.27 (2020-05-06)
## Major Changes  
- Added parameter `peptide.once.per.group` to `indexGroups()` (and also wrapper function `epfind()`) to control whether or not to restrict epitope groups to a maximum of one occurrence of a given peptide. Default value TRUE.  
- `epfind()` now write a log file to capture session info and input parameters.   

## Minor changes  
- More uniformly included `close(pb)` to conclude instances of `pb <- utils::txtProgressBar(...)` or `pb <- epitopefindr::epPB(...)`.
- epitopeSummary output table sorting modification. group number coerced to numeric.

# epitopefindr 1.1.26
## Breaking changes
- output table changes (fixed bug with epitope_summary$id number of rows mismatch, outputTable() function now returns a list with epitope_key and epitope_summary tables as elements, epfind() writes csvs with "NA" to fill empty cells)  

## Minor changes
- added parameter `remove.intermediates = FALSE` to epfind(). If set to true, then the /intermediate_files/ folder is deleted from epitopefindr's output directory at the end of the run.

# epitopefindr 1.1.25
## Minor changes
- Added support for command line utility pdfunite as an alternative to pdftk.
- Removed some defunct code and comments.
- Beginnings of framework for parallelization.