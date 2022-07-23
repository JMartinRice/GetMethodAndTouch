# GetMethodAndTouch

Attempts to deduce method name and touch details from a Hawkear .csv file.

Command line application. Takes input file name (complete path, or just file name if in current directory) and output file name (complete path, or just file name for placing in current directory) as parameters.  Output file name must have a 3-letter extension, e.g. .txt.  
Generates <OutputFileName>.txt, which contains the name(s) of the method(s) being rung, the number of the row on which the changes start (the 'M' row), the number(s) of any rows where calls are made (the 'B' or 'S' rows), the number(s) of any rows where changes to the method are made (further 'M' rws), and the numnber of the end row (the 'E' row), i.e. the row where the final rounds is first rung. 
If GMAT is unable to analyse the ringing then <OutputFileName>.txt will contain error warnings, each one preceded by '!!!'.
Also generates <OutputFileName>.pnl, which is a list of the places made at each row of the touch.  Rows in which rounds are rung are denoted 'R'.  Rows in which all bells swap are denoted '-'.  Rows which are lead ends have the letter 'L' appended to the place notation.  Similarly, calls rows have 'B' or 'S' appended. If rounds occurs on a row with 'L', 'B', or 'S' already appended then the 'R' is not added, otherwise an 'R' is appended to the PN of the first row of the final rounds.  Sunsequent rounds rows are deignated 'R'  The PN's in the PN list are separated by . (period).  The number of initial 'R's in the PN list is one less than the number of initial rounds rung.  (The last one is replaced by the PN that generates the first change.
Also generates <OutputFileName>.row, which lists the rows that should have been rung, had no method mistakes been made.
If GMAT is unable to analyse the ringing then <OutputFileName>.pnl and <OutputFileName>.row are created with zero content.

If the parameter count is incorrect returns version number.

Requires CCCBR_lib folder (and contents) to reside in current directory.
