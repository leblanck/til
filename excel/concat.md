# Concatenate Strings

Recently needed to add a new string value to the stand and end of a value in a cell. I needed this for 350+ cells. Use the `=CONCAT` formula.  

Starting Cell:
```
A1: EXAMPLE TEXT
```

Formula example:
```
=CONCAT("<string>",A1,"</string>")
```

Returns:
```
A1: <string>EXAMPLE TEXT</string>
```

*source:* [stack overflow](https://stackoverflow.com/questions/72004741/add-specific-characters-before-and-after-every-cell-val)
