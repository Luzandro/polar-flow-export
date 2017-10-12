# polar-flow-export
Cross plattform tool for bulk exporting TCX files from [Polar Flow](https://flow.polar.com/). GUI for the command line tool from [Gabriel Reid](https://github.com/gabrielreid/polar-flow-export), slightly modified to make the TCX files compatible with [Garmin Connect](https://connect.garmin.com/).

Requires [Python 2.7](https://www.python.org/downloads/) (will *not* work with 3.X)

## Simple instruction for GUI

After installing Python 2.7, download [this zip](https://github.com/Luzandro/polar-flow-export/archive/master.zip), extract it and run polarflowexport.py

By default will export everything from the given start date until today to the folder "tcx_export" in the current working directory. 

## Alternative command line interface

Alternative to using the GUI, you can also pass the arguments on the command line, where you have a few more options:

    python polarflowexport.py <username> <password> <start_date> <end_date> <output_dir> [make_garmin_compatible]

The start_date and end_date parameters are ISO-8601 date strings (i.e.
year-month-day). An example invocation is as follows:

    python polarflowexport.py me@me.com mypassword 2015-08-01 2015-08-30 /tmp/tcxfiles

If the optional parameter *make_garmin_compatible* is set to true, [the Creator and Author section of the downloaded tcx files will be stripped away](https://forums.garmin.com/forum/into-sports/garmin-connect/79753-polar-flow-tcx-export-to-garmin-connect), so that garmin connect accepts the files (when using the GUI it is always stripped away).


Licensed under the Apache Software License v2, see: http://www.apache.org/licenses/LICENSE-2.0

This project is not in any way affiliated with Polar or Polar Flow. It is purely a
hobby project created out of a need to export a large quantity of TCX files from 
Polar Flow.
