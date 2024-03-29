# Windows-Log-Analyser

A set of python scripts to analyse, present and visualise Windows .evtx log files
This was an assignment I completed for university. 

--

If you're going to copy this, make a contribution / pull request to make it better ;) Some ideas:
 - Remove all os.system() cus thats gross and not secure - you can import it as a local library instead. 
 - Make a better loading bar, cus thats also gross.
 - Create a .pdf / .html report.
 - Use 'f strings' instead of appending strings together, cus that's gross.
 - Import a logging module instead of using the one I created
 - why sys.exit()?
 - Find a way to remove all duplicate lines of scanning through files. Duplicate code is gross...
 - Produce different kinds of graphs?

## Dependencies

 - Python3
 - Evtx (pip3 install python-evtx)

## Getting Started

To start, unzip the example log files in the .7z archive, or use your own.
You should have all the python (.py) files and .evtx files in /evtx_logs.

run hello.py, there will be a menu:

- python3 hello.py

## Script Functions

convert.py - Check and clear any existing xml files before converting .evtx event log files to .xml files for analysis.

analyse.py - Search for specific event IDs in any .xml files found. Please note: you will not be able to run this without any existing .xml files.

visualise.py - Visualise a log file from analyse.py. Please note: you will not be able to run this without any analyse.py logs.

Event ID information - Search for IDs or terms for descriptions of events. 
Ref: www.ultimatewindowssecurity.com/securitylog/encyclopedia/

View Logs - View any log files created from convert.py, analyse.py and visualise.py without having to come out of the script. There is a plaintext datasheet file in the main directory that belongs to this script. This contains all the relevant security logs with descriptions.

## Files

CI5235_Logs - All scans made will be logged to this directory. You can view them via the "View Logs" menu item or just look in this directory yourself.

evtx_logs - This directory is reserved for the .evtx log files. These will be the files being analysed by the scripts. You can add or remove any. There are some example .evtx files already.

evtx_dump.py - Used for converting evtx to xml. https://github.com/williballenthin/python-evtx

## Example Usage

Convert   - 00:05

Analyse   - 01:15

Visualise - 01:22 ( Visualisation shown on seperate window, see below for example )

Event DB  - 01:40

View Logs - 02:00

[![asciicast](https://asciinema.org/a/340139.svg)](https://asciinema.org/a/340139)

**Visualise example**:

![visdata](https://imgur.com/1VJwx9v.png)
