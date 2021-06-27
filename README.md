'birddog' (at current version 0.7) is a PowerShell function for parsing a .csv or .json file for a search term and 
identifying the lines where that term occurs.  The intended use-case is for identifying the location of a string for manual
manipulation where automatically replacing every occurrence of the string within the file with powershell is 
unwanted.
Once 'birddogv0.7.ps1' is run within a PowerShell session, the function can be invoked in one of two ways;  By
feeding the 'filepath' and 'searchterm' parameters on the same line:

PS C:\> birddog -filepath C:\example.csv -searchterm UserImLookingFor

Or via invoking the function, and giving the 'filepath' and 'searchterm' parameters as prompted:

PS C:\> birddog
cmdlet birddog at command pipeline position 1
Supply values for the following parameters:
filepath: C:\example.csv
searchterm: UserImLookingFor

Note: Birddog can be piped into Format-Table to clean up results if necessary:

PS C:\> birddog -filepath C:\example.csv -searchterm UserImLookingFor | Format-Table -Autosize

As of v0.7 only .csv and .json files are supported.  Further development to enable .xls and .xlsx parsing is intended.
Thank you for reading!
