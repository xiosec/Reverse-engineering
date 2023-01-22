Ollydbg plugin - Data Ripper 1.21

26th February 2006 - 1.21 release

1) fixed window handle bug

28th January 2006 - 1.2 release

1) Improved handling of Ollydbg close when Data Ripper is open.
2) Compatiblity with Ollydbg Shadow
3) Data Ripper dialog stays on top (option) 


17th January 2006 - 1.1 release

1) "Data Ripper" menu added to dissassembler window. Code bytes can now be ripped as data.
2) Added option to override the warning to save file.
3) Added option to rip data immediately Data Ripper is launched using previous settings.
4) Added "Apply" function to Settings dialog.
5) Handled issue with multiple plugin instances.



10th January 2006 - first release

Data Ripper is an easy way to rip any kind of data from an app being debugged using Ollydbg. The ripped data can be formatted and "declared" in the syntax of the popular programming languages MASM, C/C++ and Delphi.

Data Ripper is useful whenever you need to rip data, tables etc out of an app so the data can be used in another compiled program.


NOTES

1) To install copy DataRipper.dll to the Ollydbg plugin directory

2) Data Ripper maintains settings between debugging sessions in the Ollydbg.ini file. Temporary data is stored in a file DataRipper.tmp. 

3) Data Ripper can rip data up to the Windows size limit.



HELP

Basic Use

1) Highlight the data to be ripped in any memory window of Ollydbg.

2) Right click and select "Data Ripper" in the Ollydbg popup window

3) The Data Ripper dialog will popup with an empty file "untitled"

4) Select the "Settings" dialog and check the "Language" "Format" and other settings are ok. You can specify

	Language  : ASM, C/C++, Delphi, Comma Separated Values CSV or Data String.
	"Declare" : indicates whether the programming language declaration information header
                    and trailer are required
	Format    : select bytes, words or dwords. Note if the number of data bytes selected in Ollydbg
                    does not correspond exactly with the word or dword format setting, trailing bytes
                    are set to zero.
	Hex       : if set output is in hexadecimal otherwise decimal
	Items/Line: how many bytes, words, dwords per line (Max 255)
	Indent    : spaces indented on each line (max 255)
	
5) Press "Rip Data" and the app data will be ripped and formatted into a Data Ripper file.

6) Data Ripper provides basic "richedit" editing functions. After any editing, merging with other files etc is done, save the ripped data file.

7) If you want to change the langugage, format, items/line etc, open up the "Settings" dialog, "Save" the new settings and press "Rip Data" again. Data Ripper will ask you if you want the save the file that is already there before the reformatted data is displayed.

8) Close Data Ripper.


Report any problems to http://www.sndforum.da.ru

Ziggy
January 2006

