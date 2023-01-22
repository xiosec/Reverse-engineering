Ollydbg plugin - Code Ripper 1.2

26th February 2006 - Release 1.2

- added option to insert a blank line before/after procedures and/or labels
- fixed window handle bug
- fixed handling of FFFFFFFx constants


31st January 2006 - first release 1.1

Code Ripper is an easy way to rip disassembled assembler code from an app being debugged using Ollydbg. The ripped code can be formatted and saved in the syntax of the popular programming languages MASM, C/C++ (inline ASM)  and Delphi (inline ASM). 

Code Ripper prepares the disassembled code as far as possible for easy editing and compilation. The syntax of the ripped assembler statements conforms to the selected compiler systax but, of course there are limits to what can be done to a ripped code snippet to fix all address, data references etc so the code can be compiled. Some manual interpretation and fixing will usually be required.

Features

1) Rips selected code from Ollydbg disassembler window and formats according to MASM, C/C++ (in line assembler) or Delphi (inline assembler) syntax. NOTE : Ideal (Borland) and HLA (Randall Hyde) assembler syntax should work too but have not been fully tested.

2) Ollydbg comments and user comments can be ripped with the code (option).

3) Code Ripper creates labels for call and jump destinations within the code snippet. The labels include the module name and assembler address value making it easier to cross reference those call/jump destinations back to the Ollydbg disassembler and debugged application. Symbolic addresses will be used where defined.

4) Where call/jumps and call/jump destinations are inside the code snippet, Code Ripper resolves the addresses and creates the labels with the correct language syntax.

5) Where call/jump destinations are outside the code snippet, Code Ripper will warn (option) that the address is not resolved. This makes it easier to identify other code snippets which are required or to fix those addresses manually before compiling. Calls to other modules and system APIs are identified by module name. If other code snippets are ripped, the call/jumps addresses and labelled destinations in one snippet will align with the call/jump addresses and labelled destinations in another. This makes it a lot easier to rip code snippets which may be at addresses scattered through a debugged app. In other words, a number of code snippets from one app can be more easily combined and compiled. 
  
6) Unresolved jump and call destinations will need to be corrected by hand. Code Ripper flags (option) any unresolved addresses. Where necessary, labels are created which align with the assembler code addresses.

7) Procedure start and end statements (as analysed by Ollydbg) can be flagged (option)

8) Data references include module name and address making it easier to identify what data declarations are required to compile the code and to cross reference data references back to the debugged application.

9) Code and labels can be formatted (option) to ident a selected number of spaces (max 255).

10) Comments and warnings can be formatted (option) to start at a selected column (max 255)

11) Option to format code Upper/Lower case or as code is disassembled by Ollydbg

12) Option to insert a blank line before/after procedures and labels.


NOTES

1) To install copy CodeRipper.dll to the Ollydbg plugin directory

2) Code Ripper maintains settings between debugging sessions in the Ollydbg.ini file. Temporary data is stored in a file CodeRipper.tmp. 

3) Code Ripper can rip code up to the Windows size limit.

4) For best results there are 3 Ollydbg disassembler options which should be set for Code Ripper

    Ollydbg Debugging Options - Disasm Tag

	- Disassembling syntax - select MASM (Microsoft)  Note: Ideal (Borland) and HLA (Randall Hyde) should
                                                          work but have not been fully tested
	- check "Show local module name"
	- check "Show symbolic addresses"

	other options can be set as required


HELP

Basic Use

1) Highlight the code to be ripped in the disassembler window of Ollydbg.

2) Right click and select "Code Ripper" in the Ollydbg popup window

3) The Code Ripper dialog will popup with an empty file "untitled". (If the option "Rip code at launch" is set, the code is ripped immediately - skips step 4 and 5)

4) Select the "Settings" dialog and check the "Language" "Format" and other settings are ok. You can specify

	Language     : ASM, C/C++, Delphi.
	Indent       : The number of spaces to indent for Code and/or Labels can be set. (Max 255 spaces)
	Comments     : If set, user and Ollydbg comments are copied over from the Ollydbg disassembler.
        Warnings     : If set, Code Ripper flags any unresolved addresses, indicates the start and
                       end of procedures and embedded data.
	Column       : Specifies the column to be used for the start of Comments and Warnings
        Code Format  : If set to "Ollydbg" the code is formatted upper or lower case as in the Olly disassembler
                       window. The Code Ripper Upper or Lower Case setting overrides the Ollydbg format.
        Insert Line  : Option to insert a blank line before and/or after procedures and labels.   
	
5) Press "Rip Code" and the app code will be ripped and formatted into a Code Ripper file.

6) Code Ripper provides basic "richedit" editing functions. After any editing, merging with other files etc is done, save the ripped code file. Code Ripper window also supports "drag and drop".

7) If you want to change the programming language, indent, Comments, warnings etc, open up the "Settings" dialog. New settings can be saved or applied to the ripped code. Settings are remembered for the next Code Ripper launch.

8) Code Ripper will warn you if you want to change any file that is already ripped without saving the code. This warning can be turned off under the "Settings" menu.

9) Close Code Ripper.


Thanks to diablo2oo2 for beta testing and suggestions for improvements.


Report any problems to http://www.sndforum.da.ru


Ziggy
January 2006

