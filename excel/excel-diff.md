# Getting a Diff of two columns in Excel

I recently needed to find what values were duplicates/diffs between two columns of data (think long list of Serial Numbers, etc). The following forumat can be put into Column C and copied down to take the vlaue in Column A and look for a duplicate in Column B. These can be swaped if needed. 

```
=IF(ISERROR(MATCH(A1,$B$1:$B$10000,0)),"Unique","Duplicate")
```
